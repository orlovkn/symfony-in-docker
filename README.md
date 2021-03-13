Symfony Clean Template
===

### build project
```
docker-compose up --build -d
```

### enter into php container
```
docker exec -it symfony-app-php-cli bash
```

### install Symfony
```
composer create-project symfony/website-skeleton app
```

### afterinstallation enter all these commands
```
mv /symfony/app/* /symfony
mv /symfony/app/.* /symfony
rm -Rf app
```

### run server and app
```
php -S localhost:8081
```