## About Project

Laravel Study is a project to execute and learn new things in laravel.
This project is installed using Laravel Sail.

# Getting started

## Installation
Please check the official laravel installation guide for server requirements before you start. [Official Documentation](https://laravel.com/docs/8.x/installation#installation)

Alternative installation is possible without local dependencies relying on [Sail](#sail). 

Clone the repository

    git clone https://github.com/saeedeldeeb/my-inspiring-app.git

Switch to the repo folder

    cd laravel-study

Install all the dependencies using composer

    composer install

Copy the example env file and make the required configuration changes in the .env file

    cp .env.example .env

Generate a new application key

    php artisan key:generate


## Docker

To install with [Docker](https://www.docker.com/get-started), run following commands:

```
git clone https://github.com/saeedeldeeb/my-inspiring-app.git
cd laravel-study
cp .env.example .env
docker run --rm -v "$pwd":/app composer install
docker-compose up -d
docker-compose exec app php artisan key:generate
docker-compose exec db bash
// Into DB bash
mysql -u root -p
GRANT ALL ON laravel.* TO 'laraveluser'@'%' IDENTIFIED BY 'your_laravel_db_password';
FLUSH PRIVILEGES;
EXIT;
exit
docker-compose exec app php artisan migrate
```

## Packages

- [Laravel Modules](https://nwidart.com/laravel-modules/v6/introduction)

## Dev Packages