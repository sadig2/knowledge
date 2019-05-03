[link to apache2 installation](https://www.linuxbabe.com/opensuse/apache-mariadb-php7-lamp-opensuse-leap-42-2)


sudo zypper in  php7 php7-pgsql php7-mysql apache2-mod_php7 

Then enable PHP module and restart Apache web server.
sudo a2enmod php7

sudo systemctl restart apache2
