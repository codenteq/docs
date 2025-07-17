# Installation

## Composer Installation

Run the following commands in your project directory:

```shell
composer create-project codenteq/laerx
cd laerx
composer install
php artisan storage:link
```

## Docker Installation

Alternatively, you can use Docker:

```shell
docker run --rm \
  -u "$(id -u):$(id -g)" \
  -v $(pwd):/var/www/html \
  -w /var/www/html \
  laravelsail/php81-composer:latest \
  composer install --ignore-platform-reqs
```

Link storage:

```shell
./vendor/sail/bin artisan storage link
```
