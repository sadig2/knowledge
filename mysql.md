
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


## mysql for ubuntu  
(mysql for ubuntu)[https://support.rackspace.com/how-to/installing-mysql-server-on-ubuntu/]  

## to set new root name and password   
UPDATE mysql.user SET authentication_string = PASSWORD('password') WHERE User = 'root';  
FLUSH PRIVILEGES;
## create user 
INSERT INTO mysql.user (User,Host,authentication_string,ssl_cipher,x509_issuer,x509_subject)
VALUES('demouser','localhost',PASSWORD('demopassword'),'','','');  

GRANT ALL PRIVILEGES ON demodb.* to demouser@localhost;  

 ## list users
    select User from mysql.user;
    



