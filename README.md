# laravel-toolbox

## Setup Cloned Laravel Project

https://devmarketer.io/learn/setup-laravel-project-cloned-github-com/

## If receiving you are running PHP 7 and you see the install PHP 8 error, run the following command

composer install --ignore-platform-reqs

## If PHP is out of date for the Laravel Project, Update PHP using Homebrew

## Update Homebrew

### Update homebrew
brew update

### Add the tap
brew tap shivammathur/php

### Install PHP 8.0
brew install shivammathur/php/php@8.0




# Maybe try

The most important thing to do when cloning a laravel project is to first run "composer update" then "composer install --ignore-platform-reqs". The composer install command installs any required dependencies for that laravel app.

The steps I took to clone a laravel project required the "php artisan key:generate" command. I can see in my .env file that there is an updated APP_KEY=base64:xxxxxxxxxxxxxxxxxxxx after running this command.
