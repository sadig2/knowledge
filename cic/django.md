##  enabled-sites apache configuration
    <VirtualHost 192.168.14.139:80>
            WSGIDaemonProcess 192.168.14.139 python-path=/var/www/request/request/src/
            WSGIScriptAlias / /var/www/request/request/src/muypicky/wsgi.py \
                process-group=192.168.14.139 application-group=%{GLOBAL}
            <Directory /var/www/request/request/src/muypicky>
                    <Files wsgi.py>
                            Require all granted
                    </Files>
            </Directory>
    
            Alias /static /var/www/request/request/static
            Alias /media /var/www/request/request/media_cdn
    
            ErrorLog ${APACHE_LOG_DIR}/error.log
            CustomLog ${APACHE_LOG_DIR}/access.log combined
    </VirtualHost>