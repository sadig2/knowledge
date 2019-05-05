# set apache directory
go to /etc/apache2/vhosts.d> here create vhost.conf or any other file with .conf extension.
next paste there   


\<VirtualHost *:80>  
  ServerName www.example.com  
  DocumentRoot /home/clanzu2/mypage  
  ServerAdmin webmaster@example.com  
  ErrorLog /var/log/apache2/www.example.com_log  
  CustomLog /var/log/apache2/www.example.com-access_log common  
  <Directory "/home/clanzu2/mypage">  
  Require all granted  
  \</Directory>  
  \</VirtualHost>    


then systemctl restart apache2