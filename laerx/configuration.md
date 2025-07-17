# Configuration

After installation, configure your environment variables in the `.env` file:

## If using **Docker (Laravel Sail)**:

```env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=laerx
DB_USERNAME=sail
DB_PASSWORD=password
```

Then, run:

```shell
./vendor/bin/sail artisan migrate --seed
```

## If using **Composer (Local PHP)**:

```env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=laerx
DB_USERNAME=root
DB_PASSWORD=
```

Then, run:

```shell
php artisan migrate --seed
```
