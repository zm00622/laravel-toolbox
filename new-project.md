1) Verify composer

Verify that composer is installed globally on the system by typing composer on terminal.

2) Install Laravel with Composer

A simple command needs to be executed in order to install Laravel on MacOS.

$ composer global require "laravel/installer"  

How to install Laravel on MacOS
3) Edit bash profile

To run Laravel globally on terminal, we need to edit bash profile. Type the following command to open bash-profile in vieditor.

$ vi ~/.bash_profile  
And add the following line to the file.

$ export PATH=~/.composer/vendor/bin:$PATH  

Next, create a new directory (i.e., folder to contain your project). You can use the mkdir command or create it physically.

Next, type:

laravel new projectnamehere

