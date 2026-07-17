# School Management

A **Sistem Informasi Akademik (SIAKAD)** — Academic Information System — built with [Laravel](https://laravel.com/) 7 (PHP). It includes Excel import/export, PDF generation, DataTables-driven listings, and SweetAlert-based UI notifications.

> This repository's existing README was the default, unedited Laravel framework boilerplate and didn't describe the app itself. The summary and feature list below are inferred from `composer.json` and the project structure — update the specifics (what academic data is managed: students, courses, grades, schedules, etc.) once confirmed.

## Tech Stack

- **Backend:** PHP ^7.2.5, Laravel Framework ^7.0
- **Frontend:** Blade templates, Laravel Mix (Webpack) — see `webpack.mix.js` and `package.json`
- **Database:** Laravel's Eloquent ORM (see `database/` for migrations/seeders)

### Key packages

| Package | Purpose |
|---|---|
| `maatwebsite/excel` | Importing/exporting data to and from Excel |
| `barryvdh/laravel-dompdf` | Generating PDF documents |
| `yajra/laravel-datatables-oracle` | Server-side DataTables integration |
| `realrashid/sweet-alert` | SweetAlert-based flash messages/notifications |
| `fruitcake/laravel-cors` | CORS handling |
| `doctrine/dbal` | Database schema introspection (used for certain migration operations) |

## Requirements

- PHP >= 7.2.5
- Composer
- Node.js & npm
- A database supported by Laravel (MySQL, etc.)

## Installation

```bash
git clone https://github.com/FannyDevz/Siakad-Task.git
cd Siakad-Task

# Install PHP dependencies
composer install

# Install JS dependencies
npm install

# Copy the environment file and generate an app key
cp .env.example .env
php artisan key:generate
```

Update your `.env` file with your database credentials and any other required configuration, then run the migrations:

```bash
php artisan migrate --seed
```

Build the frontend assets:

```bash
npm run dev
# or for production
npm run prod
```

## Running the App

Start the local development server:

```bash
php artisan serve
```

The app will be available at `http://localhost:8000` by default.

## Project Structure

```
.
├── app/                  # Application code (models, controllers, etc.)
├── bootstrap/            # Framework bootstrap files
├── config/                # Configuration files
├── database/              # Migrations, seeders, factories
├── public/                 # Publicly accessible entry point & assets
├── resources/                # Blade templates, frontend assets
├── routes/                     # Route definitions
├── storage/                     # Logs, compiled views, uploaded files
├── tests/                         # PHPUnit tests
├── artisan                         # Laravel CLI
├── composer.json
├── package.json
└── webpack.mix.js
```

## Testing

```bash
php artisan test
# or
vendor/bin/phpunit
```

## License

This project is built on the Laravel framework, which is open-sourced under the [MIT license](https://opensource.org/licenses/MIT). Check with the repository owner for the license terms of the application code itself, as none is specified in the repository.
