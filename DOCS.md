PACKAGE INSTALLATION
sudo apt install nginx mariadb-server mariadb-client php7.2 php7.2-fpm
sudo service nginx start
sudo service mysql start
sudo service php7.2-fpm start
curl -4 icanhazip.com
sudo mysql_secure_installation

NGINX SERVER SETUP
cd /etc/nginx/sites-available/
sudo touch midtest
sudo cp default midtest
sudo nano midtest
sudo nginx -t
sudo service nginx reload

sudo ln -s /etc/nginx/sites-available/midtest /etc/nginx/sites-enabled
sudo unlink /etc/nginx/sites-enabled/default

sudo service nginx reload

cd /var/www/html/
sudo nano info.php
sudo rm info.php


