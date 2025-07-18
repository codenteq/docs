---
sidebar_position: 2
---

# Installation

## Composer Installation

1. Require the package using Composer:

   ```shell
   composer require codenteq/iyzico-payment-gateway
   ```

2. Run autoload:

   ```shell
   composer dump-autoload
   ```

3. Add your Iyzico credentials to your `.env` file:

   ```env
   IYZICO_API_KEY=
   IYZICO_SECRET_KEY=
   IYZICO_BASE_URL=
   ```

4. Optimize your Laravel project:

   ```shell
   php artisan optimize
   ```

## Installation Without Composer

1. Unzip the extension and merge the `packages` and `storage` folders into your Laravel project's root directory.

2. In `config/app.php`, add the following to the `providers` array:

   ```php
   Webkul\Iyzico\Providers\IyzicoServiceProvider::class,
   ```

3. In `composer.json`, add the following under the `autoload.psr-4` section:

   ```json
   "Webkul\\Iyzico\\": "packages/Webkul/Iyzico/src"
   ```

4. Run the following command:

   ```shell
   composer dump-autoload
   ```

5. Update your `.env` file with Iyzico credentials:

   ```env
   IYZICO_API_KEY=
   IYZICO_SECRET_KEY=
   IYZICO_BASE_URL=
   ```

6. Optimize the project:

   ```shell
   php artisan optimize
   ```
