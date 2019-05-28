# Social_Media LSAPP
Project for M133

This project contains a social media platform for the TBZ school.

## Installation
If you want to work with this code, there are a few things you have to do first: 

### Requirements
Make sure your local environment fulfills the following requirements:
* XAMPP Apache (PHP >= 7.1.3)
    - https://www.apachefriends.org/de/index.html
* Composer
    - https://getcomposer.org/Composer-Setup.exe
* GitBash
    - https://git-scm.com/download/win
* MySQL Database
    - https://dev.mysql.com/downloads/installer

### Install Composer
Composer is a dependency manager for PHP. Make sure you have it installed.
> https://getcomposer.org/download

Follow the Instructions from the Install-Wizard.

### Install Git
At its core, Git is a set of command line utility programs that are designed to execute on a Unix style command-line environment.
> https://git-scm.com/downloads

Follow the Instructions from the Install-Wizard.  
If you get to **"Adjust your PATH environment"** change the default option to:  
**"Use Git and optional Unix tools from the Windows Command Prompt".**

### Create new Laravel Project
1. Start GitBash
2. "cd c:xampp/htdocs"
3. "composer create-project laravel/laravel [name]"

### Use This Project
1. Clone Project to C://xampp/htdocs/
2. Start GitBash
3. "cd c:xampp/htdocs"
4. "composer install"

### Create Virtual Host
Add following Lines to the end of the File:

> C:\xampp\apache\conf\extra\httpd-vhosts.conf 

    <VirtualHost *:80>
        DocumentRoot "C:/xampp/htdocs"
        ServerName localhost
    </VirtualHost>
    
    <VirtualHost *:80>
        DocumentRoot "C:/xampp/htdocs/lsapp/public"
        ServerName lsapp.dev
    </VirtualHost>

> C:\Windows\System32\drivers\etc\hosts  

    127.0.0.1 localhost
    127.0.0.1 lsapp.dev
    
New Project URL: **lsapp.dev**

## DataBase

    CREATE USER 'laravel'@'localhost' IDENTIFIED BY '1234567890';
    GRANT ALL PRIVILEGES ON * . * TO 'laravel'@'localhost';