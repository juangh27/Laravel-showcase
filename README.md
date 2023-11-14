# Laravel Docker

## Commands

```bash
docker-compose exec php-apache /bin/bash
```

```bash
composer create-project laravel/laravel .
composer create-project --prefer-dist laravel/laravel . && chown -R www-data:www-data .
```

### Copy your env mysql data to the env from laravel
