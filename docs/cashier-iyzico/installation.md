---
sidebar_position: 2
---

# Installation

First, install the Cashier package for Iyzico using the Composer package manager:

```shell
composer require codenteq/cashier-iyzico
```

After installing the package, publish Cashier's migrations using the vendor:publish Artisan command:

```shell
php artisan vendor:publish --tag="cashier-migrations"
```

Then, migrate your database:

```shell
php artisan migrate
```

Cashier's migrations will add several columns to your `users` table. They will also create a new `subscriptions` table to hold all of your customer's subscriptions with multiple prices.

If you wish, you can also publish Cashier's configuration file using the vendor:publish Artisan command:

```shell
php artisan vendor:publish --tag="cashier-config"
```