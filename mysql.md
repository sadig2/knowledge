
sudo zypper install mysql
sudo systemctl enable mysql

Verify that MySQL is enabled.
Copy
systemctl is-enabled mysql

sudo reboot

ssh 10.111.112.113

mysql_secure_installation

Sign in to MySQL
You can now sign in and enter the MySQL prompt.
mysql -u root -p

This switches you to the MySQL prompt where you can issue SQL statements to interact with the database.
Now, create a new MySQL user.
CREATE USER 'mysqluser'@'localhost' IDENTIFIED BY 'password';



mysql -u root -p
GRANT ALL PRIVILEGES ON *.* TO 'username'@'localhost' IDENTIFIED BY 'password';

show databases ;
show tables;


desc ‘table name’ ;     

