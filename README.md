# laravel-toolbox

## Laravel Directory / File Hierarchy Explained:

https://www.devsenv.com/tutorials/directory-structure-of-laravel-application-2




# ---- Everything below this line concerns errors when cloning a project. ---- 

## Setup Cloned Laravel Project

https://devmarketer.io/learn/setup-laravel-project-cloned-github-com/

## If receiving you are running PHP 7 and you see the install PHP 8 error, run the following command

composer install --ignore-platform-reqs

## If PHP is out of date for the Laravel Project, Update PHP using Homebrew (You must first install Homebrew)

## Update Homebrew

### Update homebrew
brew update

### Add the tap
brew tap shivammathur/php

### Install PHP 8.0
brew install shivammathur/php/php@8.0

### After running the above, I had to force switch to PHP 8
brew link --overwrite --force php@8.0

# Maybe try

The most important thing to do when cloning a laravel project is to first run "composer update" then "composer install --ignore-platform-reqs". The composer install command installs any required dependencies for that laravel app.

The steps I took to clone a laravel project required the "php artisan key:generate" command. I can see in my .env file that there is an updated APP_KEY=base64:xxxxxxxxxxxxxxxxxxxx after running this command.

# Use valet server

https://laravel.com/docs/8.x/valet

# Valet server install instructions

https://medium.com/modulr/how-to-install-laravel-valet-on-mac-f061ce2d095e

# Things to try

### Make sure the ~/.composer/vendor/bin directory is in your system's "PATH".

### I can ping the server

Once Valet is installed, try pinging any *.test domain on your terminal using a command such as ping foobar.test. If Valet is installed correctly you should see this domain responding on 127.0.0.1.

### Command used to set up existing laravel repo with docker

After the project has been created, you can navigate to the application directory and start Laravel Sail. Laravel Sail provides a simple command-line interface for interacting with Laravel's default Docker configuration:

cd example-app

./vendor/bin/sail up

### If you are receiving a curl error, try installing curl (you must have homebrew to use this command):

Install command:

brew install curl

### If all else fails, try loading / cloning a simple laravel project (to at least see if you can get that up and running)

### If you can run a simple laravel site, then there must be something wrong with the directory for the project you are trying to clone. 

### Check your environment configuration in .env

https://www.digitalocean.com/community/tutorials/understanding-laravel-environment-variables


