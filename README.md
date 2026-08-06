# client-server-week02-laravel-setup

## Student Information
| Field | Details |
|---|---|
| **Name** | Justin Plantilla |
| **Student No.** | 2023-12345 |
| **Course** | Bachelor of Science in Information Technology |
| **Section** | BSIT 3-A |
| **Subject** | Web Systems and Technologies |

## About This Project
A Laravel web application set up as part of Week 02 - Client-Server laboratory activity.

## Requirements
- PHP >= 8.2
- Composer
- Git
- Node.js & NPM

## Installation
```bash
git clone https://github.com/<your-username>/client-server-week02-laravel-setup.git
cd client-server-week02-laravel-setup
composer install
cp .env.example .env
php artisan key:generate
php artisan migrate
php artisan serve
```

## Screenshots
| Screenshot | Description |
|---|---|
| `screenshots/php-version.png` | PHP version |
| `screenshots/composer-version.png` | Composer version |
| `screenshots/laravel-version.png` | Laravel version |
| `screenshots/git-version.png` | Git version |
| `screenshots/mysql-version.png` | MySQL version |
| `screenshots/vscode.png` | VS Code setup |
| `screenshots/artisan-serve.png` | Running `php artisan serve` |
| `screenshots/hello-laravel-homepage.png` | Laravel homepage with student info |

## Repository Structure
```
client-server-week02-laravel-setup/
│
├── app/
├── bootstrap/
├── config/
├── database/
├── public/
├── resources/
├── routes/
├── screenshots/
│   ├── php-version.png
│   ├── composer-version.png
│   ├── laravel-version.png
│   ├── git-version.png
│   ├── mysql-version.png
│   ├── vscode.png
│   ├── artisan-serve.png
│   └── hello-laravel-homepage.png
│
├── README.md
├── .gitignore
└── LICENSE
```

## License
This project is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).
