# client-server-week02-laravel-setup

## Student Information
| Field | Details |
|---|---|
| **Name** | Justin Plantilla |
| **Student No.** | 2023-12345 |
| **Course** | Bachelor of Science in Information Technology |
| **Section** | BSIT 3-A |
| **Subject** | Web Systems and Technologies |

---

## 1. Project Title

**Week 02 – Laravel Project Setup: Client-Server Web Application Development**

---

## 2. Introduction

### Brief Overview of Laravel
Laravel is a free, open-source PHP web framework designed for building modern web applications following the Model-View-Controller (MVC) architectural pattern. Created by Taylor Otwell and first released in 2011, Laravel provides developers with an elegant syntax and a rich set of built-in tools including routing, authentication, database migrations, and templating via Blade. It is widely regarded as one of the most popular PHP frameworks due to its developer-friendly features and active community support.

### Importance of Client-Server Technologies
Client-server technology is the backbone of modern web development. In this architecture, the client (browser) sends requests to the server, which processes them and returns the appropriate response. Understanding this model is essential for any web developer because it defines how data flows between the user interface and the backend logic. Technologies like Laravel operate on the server side, handling business logic, database interactions, and dynamic content generation, while the client side renders the output for the user.

### Purpose of the Project
The purpose of this project is to set up a fully functional Laravel development environment as part of the Week 02 laboratory activity for Web Systems and Technologies. This includes installing all required tools, creating a new Laravel project, customizing the homepage with student information, and pushing the project to a public GitHub repository with proper documentation.

---

## 3. Objectives

The following objectives were achieved during this activity:

1. **Set up the development environment** by installing PHP, Composer, Git, MySQL, and VS Code on a Windows machine.
2. **Create a new Laravel project** using Composer and verify that the application runs correctly via `php artisan serve`.
3. **Customize the Laravel homepage** to display student information including name, student number, course, section, subject, and current date.
4. **Configure the MySQL database** by setting up MySQL Workbench, creating a local database, and connecting it to the Laravel project via the `.env` file and running database migrations.
5. **Initialize a Git repository** and push the complete Laravel project to a public GitHub repository with a minimum of five meaningful commits following professional commit message conventions.

---

## 4. Development Environment

| Tool | Version |
|---|---|
| **Operating System** | Windows 11 |
| **PHP** | 8.2.x |
| **Laravel** | 12.x |
| **Composer** | 2.x |
| **Git** | 2.55.0 |
| **MySQL** | 8.0.x |
| **VS Code** | Latest |

---

## 5. Installation Steps

Follow these steps to set up the project on your local machine.

### Step 1 – Verify PHP Installation
Open Command Prompt and run:
```bash
php -v
```
![PHP Version](screenshots/part1%20verify%20php.png)
*Screenshot: Verifying PHP version in the terminal.*

### Step 2 – Verify Composer Installation
```bash
composer --version
```
![Composer Version](screenshots/part2%20verify%20composer.png)
*Screenshot: Verifying Composer version in the terminal.*

### Step 3 – Install Laravel via Composer
```bash
composer create-project laravel/laravel hello-laravel
```
![Install via Composer](screenshots/part%203%20instal%20via%20composer.png)
*Screenshot: Installing Laravel project via Composer.*

### Step 4 – Verify Laravel Version
After the installation is complete, navigate into the project folder and verify the Laravel version:
```bash
cd hello-laravel
php artisan --version
```
![Laravel Version](screenshots/part3%20verify%20laravel.png)
*Screenshot: Verifying Laravel version inside the project folder using Artisan.*

### Step 5 – Verify Git Installation
```bash
git --version
```
![Git Version](screenshots/part4%20git%20version.png)
*Screenshot: Verifying Git version in the terminal.*

### Step 6 – Verify MySQL Installation
```bash
mysql --version
```
![MySQL Version](screenshots/part5%20mysql%20version.png)
*Screenshot: Verifying MySQL version in the terminal.*

### Step 7 – Open Project in VS Code
```bash
code .
```
![VS Code](screenshots/part6%20install%20vscode.png)
*Screenshot: Laravel project opened in VS Code.*

### Step 8 – Run Laravel
```bash
php artisan serve
```
Open your browser and go to `http://127.0.0.1:8000`

![Artisan Serve](screenshots/part8%20artisan%20serve.png)
*Screenshot: Running the Laravel development server.*

### Step 9 – Customize the Homepage
Edit `resources/views/welcome.blade.php` to display student information.

![Student Info Homepage](screenshots/part9%20student%20info.png)
*Screenshot: Customized Laravel homepage displaying student information.*

### Step 10 – Push to GitHub
```bash
git init
git add .
git commit -m "feat: initialize Laravel project"
git branch -M main
git remote add origin https://github.com/justinplantilla/client-server-week02-laravel-setup.git
git push -u origin main
```
![Push to GitHub](screenshots/part10%20push%20to%20github%20repo.png)
*Screenshot: Successfully pushing the project to GitHub.*

---

## 6. Project Structure

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
│   ├── part1 verify php.png
│   ├── part2 verify composer.png
│   ├── part3 verify laravel.png
│   ├── part4 git version.png
│   ├── part5 mysql version.png
│   ├── part6 install vscode.png
│   ├── part7 laravel project.png
│   ├── part8 artisan serve.png
│   ├── part9 student info.png
│   └── part10 push to github repo.png
│
├── README.md
├── .gitignore
└── LICENSE
```

### Important Folder Descriptions

| Folder | Purpose |
|---|---|
| `app/` | Contains the core application code including Models, Controllers, and Providers. This is where the main business logic of the application lives. |
| `routes/` | Defines all URL routes for the application. `web.php` handles browser routes while `api.php` handles API routes. |
| `resources/` | Contains all frontend assets including Blade template views (`views/`), CSS (`css/`), and JavaScript (`js/`) files. |
| `public/` | The web server's document root. Contains `index.php` which is the entry point for all HTTP requests, along with compiled assets. |
| `config/` | Stores all configuration files for the application such as database settings, mail, cache, session, and more. |
| `database/` | Contains database migrations, seeders, and factories. Migrations define the database schema and allow version control of the database structure. |

---

## 7. Problems Encountered

During the setup of this Laravel project, the following challenges were encountered:

### Problem 1 – MySQL Connection Refused
When running the application for the first time, the following error appeared:
```
Illuminate\Database\QueryException: could not find driver
(Connection: mysql, Database: laravel)
```
This occurred because the MySQL service was not running and the `.env` file was not properly configured with the correct database credentials.

### Problem 2 – Git Not Recognized in Terminal
When attempting to run `git` commands in the terminal, the error `'git' is not recognized as an internal or external command` appeared. Git was installed but its executable path was not added to the Windows system PATH environment variable.

### Problem 3 – GitHub Authentication Failure
When pushing to GitHub using `git push`, the terminal prompted for a username and password. Using the GitHub account password resulted in a `403 Permission Denied` error because GitHub no longer accepts plain passwords for Git operations over HTTPS — a Personal Access Token (PAT) is required instead.

---

## 8. Solutions

### Solution 1 – Configure MySQL via .env and MySQL Workbench
Opened MySQL Workbench and started the local MySQL server instance. Created a new database named `laravel`, then updated the `.env` file with the correct credentials:
```ini
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=laravel
DB_USERNAME=root
DB_PASSWORD=
```
After saving the file, ran `php artisan migrate` to create the required database tables.

### Solution 2 – Use Full Git Path
Since Git was not on the system PATH, the full executable path was used for all Git commands:
```bash
"C:\Program Files\Git\cmd\git.exe" push -u origin main
```
Alternatively, Git can be added to the Windows PATH via System Properties → Environment Variables → Path → Add `C:\Program Files\Git\cmd`.

### Solution 3 – Generate a Personal Access Token (PAT)
Resolved the GitHub authentication issue by generating a Personal Access Token (PAT) from GitHub Settings → Developer Settings → Personal Access Tokens → Tokens (classic). The token was granted the `repo` scope and used as the password when pushing. The remote URL was updated to include the token:
```bash
git remote set-url origin https://justinplantilla:<token>@github.com/justinplantilla/client-server-week02-laravel-setup.git
```

---

## 9. Screenshots

| # | Screenshot | Description |
|---|---|---|
| 1 | ![](screenshots/part1%20verify%20php.png) | Verifying PHP installation and version in the terminal |
| 2 | ![](screenshots/part2%20verify%20composer.png) | Verifying Composer installation and version |
| 3 | ![](screenshots/part%203%20instal%20via%20composer.png) | Installing Laravel project via Composer |
| 4 | ![](screenshots/part3%20verify%20laravel.png) | Verifying Laravel version using `php -v` |
| 5 | ![](screenshots/part4%20git%20version.png) | Verifying Git installation and version |
| 6 | ![](screenshots/part5%20mysql%20version.png) | Verifying MySQL installation and version |
| 7 | ![](screenshots/part6%20install%20vscode.png) | VS Code editor installed and configured |
| 8 | ![](screenshots/part8%20artisan%20serve.png) | Running the Laravel development server with `php artisan serve` |
| 9 | ![](screenshots/part9%20student%20info.png) | Customized homepage by editing `welcome.blade.php` to display student information |
| 10 | ![](screenshots/part10%20push%20to%20github%20repo.png) | Successfully pushing the project to the GitHub repository |

---

## 10. Reflection

Setting up a Laravel development environment from scratch was both a challenging and rewarding experience. Before this activity, my understanding of web frameworks was mostly theoretical. Going through the actual installation and configuration process gave me a much deeper appreciation of how modern web applications are structured and deployed.

One of the most important things I learned is how a PHP framework like Laravel abstracts away much of the repetitive work involved in web development. Instead of writing raw PHP for every route, database query, or HTML template, Laravel provides a clean and organized structure that makes development faster and more maintainable. The MVC pattern, in particular, helped me understand how to separate concerns — keeping the business logic, data handling, and presentation in distinct layers of the application.

The challenges I encountered during this activity were also valuable learning experiences. The MySQL connection error taught me how to properly configure the `.env` file and start the MySQL service using MySQL Workbench. The Git PATH issue reminded me that software installation on Windows often requires manual environment variable configuration, which is a common real-world task for developers. The GitHub authentication problem introduced me to Personal Access Tokens, which are a more secure alternative to password-based authentication and are now the industry standard for Git operations over HTTPS.

Laravel is particularly important in client-server development because it provides a robust server-side framework that handles everything from routing and middleware to database migrations and session management. In a client-server architecture, the server must reliably process requests, interact with the database, and return well-structured responses. Laravel's built-in tools make all of this straightforward, allowing developers to focus on building features rather than reinventing the wheel.

This knowledge will be extremely valuable in my future software development projects. Understanding how to set up and configure a Laravel environment means I can quickly bootstrap new web applications. Knowing how Git and GitHub work together for version control means I can collaborate effectively with other developers and maintain a clean project history. Most importantly, this activity gave me confidence that I can troubleshoot real-world development issues — from missing PHP extensions to authentication errors — which is an essential skill for any professional software developer.

---

## 11. References

Laravel. (2024). *Laravel documentation*. https://laravel.com/docs

PHP. (2024). *PHP manual*. https://www.php.net/manual/en/

Composer. (2024). *Composer documentation: Dependency manager for PHP*. https://getcomposer.org/doc/

Git. (2024). *Git documentation*. https://git-scm.com/doc

GitHub. (2024). *GitHub docs: Creating a personal access token*. https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens

Otwell, T. (2024). *Laravel: The PHP framework for web artisans*. Taylor Otwell. https://laravel.com

W3Schools. (2024). *PHP tutorial*. https://www.w3schools.com/php/

---

## License
This project is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).
