# laravel-toolbox

## Laravel Directory / File Hierarchy Explained:

https://www.devsenv.com/tutorials/directory-structure-of-laravel-application-2

# Laravel for Front End Devs:

https://medium.com/@nedsoft/how-to-work-with-laravel-as-a-front-end-dev-85ac2d420da7

### Assuming you want to link public/css/style.css, public/js/script.js and public/images/avartar.jpg to a blade view, blade’s way of doing it is shown below:

``` 
<link href="{{ asset('css/style.css')}}" rel="stylesheet"> // for css asset

<script src="{{ asset('js/script.js')}}"></script> // for js asset

<img src="{{ asset('images/avartar.jpg')}}" alt=""> // for image asset

```
Once you’ve created your blade view, you might want to view it on the browser, to achieve that, you need to create a route for that particular view.

Let’s create a blade view called test.blade.php in the resoures/views directory. Add a HTML boilerplate in the test.blade.php file as shown belo:

Next, open routes/web.php and add the code below:

```
Route::get('/test', function () {
    return view('test'); // test here is the test.blade.php
});
```

You have registered the route for accessing the test.blade.php. Now open your browser and enter localhost:8000/test.

Awesome! you discover that your browser displays the content of test.blade.php.

Now let me briefly explain the route code above. Notice the return statement, Laravel ships with a helper function view() for accessing the view templates. The parameter it accepts is the name of the blade template, in our case, we name it test.blade.php and hence we pass test to the view() function as view(‘test’).

Note: if the blade template is located in a sub-directory of the reources/views

for example resources/views/email, then we can access it as view(‘email.test’).

Since you’d be needing many templates, it’d be boring and time-consuming adding routes for each blade template you create. The trick I’m going to show will enable your access all your templates with a single route using the name of the template as the route. The code is shown below:

```
Route::get(/{$route}, function (){
    
     return view($route);
});
```

Note: All the templates must be in the root directory of the resources/views for the code above to work, except you modify it to suit your directory structure.

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


