# Quickstart

1. **Install Dependencies**
   With Composer or Docker (see above).

2. **Set up `.env` File**
   Copy `.env.example` to `.env` and adjust database settings.

3. **Run Migrations and Seeders**
   Seed demo data to get started quickly:

   ```shell
   php artisan migrate --seed
   ```

4. **Serve Application**
   If using Laravel Sail:

   ```shell
   ./vendor/bin/sail up
   ```

   Or locally:

   ```shell
   php artisan serve
   ```

5. **Open in Browser**
   Visit [http://localhost](http://localhost) or your configured host.
