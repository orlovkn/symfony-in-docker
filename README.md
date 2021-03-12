## Installation
Launch the docker
```
cp .env.test .env
docker-compose up --build -d
cd app
```

### Установка Symfony

Зайти в контейнер с php:
```
docker exec -it symfony-app-php bash
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