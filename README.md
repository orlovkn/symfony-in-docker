## Installation
Launch the docker
```
cp .env.test .env
docker-compose up --build -d
cd app
```

Чтобы войти в любой из контейнеров, делаем следующее:
```
docker exec -it <container_name> bash
```

show running containers
```
docker ps
```
stop all containers
```
docker stop $(docker ps -qa)
```

Логи контейнера:
```
docker logs <container_name>
```

### Установка Symfony

Зайти в контейнер с php-cli:
```
docker exec -it symfony-app-php-cli bash
```

Выполнить команду
```
composer create-project symfony/website-skeleton app
```

После установки выполнить команды, чтобы избавиться от вложенности папок:
```
mv /symfony/app/* /symfony
rm -Rf app
```

run server and app
```
php -S localhost:8081
```