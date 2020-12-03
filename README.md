### Запуск проекта

```
cp .env.test .env
docker-compose up --build -d
cd app
cp .env.test .env
```

Чтобы войти в любой из контейнеров, делаем следующее:
```
docker exec -it <container_name> bash
```

Посмотреть запущенные контейнеры:
```
docker ps
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
mv /symfony/app/.* /symfony
rm -Rf app
```

Открыть приложение
```
localhost:8081
```