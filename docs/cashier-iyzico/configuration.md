---
sidebar_position: 3
---

# Configuration

## Billable Model

Before using Cashier, add the `Billable` trait to your billable model definition. Typically, this will be the `App\Models\User` model. This trait provides various methods to allow you to perform common billing tasks, such as creating subscriptions, applying coupons, and updating payment method information:

```php
use Codenteq\Iyzico\Billable;

class User extends Authenticatable
{
    use Billable;
}
```

## API Keys

Next, you should configure your Iyzico API keys in your application's .env file. You can retrieve your Iyzico API keys from the Iyzico control panel:

### Introduction

Here in this page, you'll have details of creating a Sandbox account and API credentials.

> If you already have a Sandbox, then please follow the [link](https://sandbox-merchant.iyzipay.com/auth/login) to login your account.

### Sign up for a Sandbox

Please following [link](https://sandbox-merchant.iyzipay.com/auth/register) to sign up a Sandbox account;

A Sandbox account offers you to manage everything from one simple panel.
Each account comes with unique merchantId as well as two pairs of credentials, `API KEY` & `SECRET KEY`, relatively.

| KEY        | VALUE         |
|------------|---------------|
| API Key    | sandbox-...   |
| Secret Key | sandbox-...   |

> For the Sandbox, OTP is 123456 statically.

### Take Your Credentials

In iyzico services, you will be asked for authentication before making any transaction.
To find out where;

1. Log in to your [Sandbox Account](https://sandbox-merchant.iyzipay.com/auth/login).
2. Follow the path **Settings > Merchant Settings** from the menu on the left.
3. Under the **Merchant Settings** page, go for API Keys section.
Once you click on **Show detail**, there are the magic begins.

```ini
IYZICO_API_KEY=
IYZICO_SECRET_KEY=
IYZICO_BASE_URL=
```

> To use the subscription feature in your application, you need to get approval for the subscription menu by contacting [email](mailto:destek@iyzico.com) or by calling the iyzico support hotline.

## Currency Configuration

The default Cashier currency is Turkis Lira (TRY). You can change the default currency by setting the `CASHIER_CURRENCY` environment variable within your application's `.env` file:

```ini
CASHIER_CURRENCY=USD
```