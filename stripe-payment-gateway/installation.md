# Installation

## Composer Installation

1. Require the package using Composer:

   ```shell
   composer require codenteq/stripe-payment-gateway
   ```

2. Run autoload:

   ```shell
   composer dump-autoload
   ```

3. Optimize your Laravel project:

   ```shell
   php artisan optimize
   ```

4. Go to the Bagisto admin panel, find the Stripe payment gateway, enter your API key and start receiving payments.

   ```url
   http://localhost:8000/admin/configuration/sales/payment_methods
   ```

5. To use the demo API key, paste the key into the Stripe Client Secret section.

   ```ini
   sk_test_BQokikJOvBiI2HlWgH4olfQ2
   ```

---

## Installation Without Composer

1. Unzip the extension and merge the `packages` and `storage` folders into your Laravel project's root directory.

2. In `config/app.php`, add the following to the `providers` array:

   ```php
   Webkul\Stripe\Providers\StripeServiceProvider::class,
   ```

3. In `composer.json`, add the following under the `autoload.psr-4` section:

   ```json
   "Webkul\\Stripe\\": "packages/Webkul/Stripe/src"
   ```

4. Run the following command:

   ```shell
   composer dump-autoload
   ```

5. Optimize the project:

   ```shell
   php artisan optimize
   ```

6. To use the demo API key, paste the key into the Stripe Client Secret section.

   ```ini
   sk_test_BQokikJOvBiI2HlWgH4olfQ2
   ```
