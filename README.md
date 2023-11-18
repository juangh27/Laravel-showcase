# Laravel Docker

## Commands

```bash
docker exec -it php-showcase /bin/bash
composer install
```

### Copy your env mysql data to the env from laravel

```bash
php artisan key:generate
php artisan migrate
```

### Optional

```bash
php artisan optimize
```

### Runing laravel server

```bash
php artisan serve
```

you can check that Laravel is running correctly [here](http://localhost:8080/).

### Extra commands

```bash
php artisan make:controller QuoteController

#if the routes arent updating or working correctly use this commands

php artisan route:clear
php artisan config:clear
```
