# STEPS TO DEPLOY LARAVEL 
#### ON DIGITAL OCEAN SERVEr

### Step 1: Install PHP
    sudo apt-get install php7.0-mbstring php7.0-xml composer unzip




## Inside mysql terminal

### Step 2:Enetr mysql as root
    mysql -u root -p

### Step 3: Create database
*mysql>* CREATE DATABASE project1 DEFAULT CHARACTER SET utf8 COLLATE utf8_unicode_ci;

### Step 4: Grant Privileges *(quotation are required)*
*mysql>* GRANT ALL ON project1.* TO 'laraveluser'@'localhost' IDENTIFIED BY 'password';

### Step 5: Flush to notify MySql server for changes
    mysql> FLUSH PRIVILEGES;




## Inside SSH

### Step 6: Install/Pull laravel files from github
    $ cd /var/www/html/folder
    $ git clone -b branchname https://github.com/laravel/quickstart-basic

### Step 7: Install the packages needed by project
    $ cd project1
    $ composer install
    $ git clone -b branchname https://github.com/laravel/quickstart-basic

### Step 8: Configur .env file for this server
    $ nano .env 
    *(use tab to write .env file name to be sure such file exists)*
    *(for first run keep env local and debug true later on change those)*

### Step 9: Database Migration and seeding
    $ php artisan migrate

    
