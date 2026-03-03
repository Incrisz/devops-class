# cmd to pull laravel new file 
composer create-project laravel/laravel project-name

# navigate to your project directory 
cd project-name 

# start the application server 
php artisan serve

# to pull laravel deps on the server
apt install nginx

apt install php
apt install php-dom
apt install php-xml
apt install composer
composer update

cp .env.example .env

php artisan key:generate

php artisan serve --host=0.0.0.0 --port=8000

# setting database
apt install mysql-server
sudo apt install php-mysql -y

mysql -u root 

CREATE DATABASE henry;

CREATE USER 'henry'@'localhost' IDENTIFIED BY 'henry';

GRANT ALL PRIVILEGES ON henry.* TO 'henry'@'localhost';

FLUSH PRIVILEGES;

exit


# migrate our tables to db
php artisan migrate


# Allow MySQL to Listen on All Interfaces
sudo nano /etc/mysql/mysql.conf.d/mysqld.cnf

# change bind-address = 127.0.0.1 to bind-address = 0.0.0.0
sudo systemctl restart mysql


# step 2 

mysql -u root 

ALTER USER 'henry'@'localhost' IDENTIFIED BY 'henry';
CREATE USER 'henry'@'%' IDENTIFIED BY 'henry';
GRANT ALL PRIVILEGES ON henry.* TO 'henry'@'%';
FLUSH PRIVILEGES;