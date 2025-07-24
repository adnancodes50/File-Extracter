Laravel File Uploader - Project Documentation
1. Project Overview
This is a Laravel-based File Uploading web application that allows users to upload and possibly manage files.
The project is structured using standard Laravel conventions and integrates Tailwind CSS for styling.
2. Features
- Secure file upload functionality
- Laravel 10+ framework
- Tailwind CSS integrated
- Vite for modern frontend asset bundling
- `.env` file for environment-based configuration
- RESTful route structure
- Easily extendable structure for additional features
3. Folder Structure
| Folder / File         | Purpose                                        |
|-----------------------|------------------------------------------------|
| app/                  | Contains core application logic                |
| bootstrap/            | Bootstrap Laravel framework and caching        |
| config/               | Application configuration files                |
| database/             | Migrations, seeders, factories                  |
| public/               | Publicly accessible files                      |
| resources/            | Blade templates, CSS, JS                       |
| routes/               | Route definitions (web.php, api.php, etc.)     |
| storage/              | Logs, cache, uploaded files                    |
| tests/                | Automated tests                                |
| .env                  | Environment configuration file                 |
| composer.json         | PHP dependencies                               |
| package.json          | NodeJS dependencies                            |
| vite.config.js        | Vite configuration for asset building          |
4. Installation Guide
1. Clone or Extract the Project
git clone <repo-url> OR extract the ZIP

2. Install PHP Dependencies
composer install

3. Install Node Modules
npm install

4. Copy .env File
cp .env.example .env

5. Generate App Key
php artisan key:generate

6. Set Permissions
chmod -R 775 storage bootstrap/cache

7. Run Migrations (if DB used)
php artisan migrate

8. Start Development Server
php artisan serve

9. Compile Frontend Assets
npm run dev
5. Usage Instructions
- Open browser at http://localhost:8000
- Use the file upload form (likely in resources/views/)
- Uploaded files stored in storage/app/public (or configured location)
6. Environment Setup (.env)
Ensure the following is set in your .env:

APP_NAME=Laravel
APP_URL=http://localhost
APP_ENV=local
APP_KEY=base64:...
APP_DEBUG=true

DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=fileupload
DB_USERNAME=root
DB_PASSWORD=

FILESYSTEM_DISK=public
7. Technologies Used
- PHP 8.x
- Laravel 10+
- Tailwind CSS
- Vite
- MySQL or SQLite
- Node.js & NPM
- Composer
8. Developer Notes
- Use Laravel’s validation for file uploads (`mimes`, `max`, etc.)
- Customize upload path in config/filesystems.php
- Run `php artisan storage:link` to link storage folder to public
