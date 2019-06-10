[article about nginx](https://www.digitalocean.com/community/tutorials/how-to-set-up-django-with-postgres-nginx-and-gunicorn-on-ubuntu-16-04)
## install packages 
    sudo apt-get install python3-pip python3-dev libpq-dev postgresql postgresql-contrib nginx


## create virtual evnvironment 
    virtualenv py1
## create django project 
    django-admin startproject djangoproj1

##  set up postgres  
    sudo -u postgres psql
    CREATE DATABASE myproject;
    CREATE USER myprojectuser WITH PASSWORD 'password';
    ALTER ROLE myprojectuser SET client_encoding TO 'utf8';
    ALTER ROLE myprojectuser SET default_transaction_isolation TO 'read committed';
    ALTER ROLE myprojectuser SET timezone TO 'UTC';
    
    sudo -H pip3 install --upgrade pip
    sudo -H pip3 install virtualenv
   
## generate virtual environment 
    virtualenv myprojectenv
##  activate the environment 
    source myprojectenv/bin/activate    
## install adaptor for postgresql  (psycopg2) 
    pip install django gunicorn psycopg2
## edit setting.py 
    DATABASES = {
        'default': {
            'ENGINE': 'django.db.backends.postgresql_psycopg2',
            'NAME': 'myproject',
            'USER': 'myprojectuser',
            'PASSWORD': 'password',
            'HOST': 'localhost',
            'PORT': '',
        }
    }
## place static files in  a directory and show in setting.py  images css js
    STATIC_URL = '/static/'
    STATIC_ROOT = os.path.join(BASE_DIR, 'static/')
## make changes in db
    ~/myproject/manage.py makemigrations
    ~/myproject/manage.py migrate   
    ~/myproject/manage.py createsuperuser
## collect photos and static files in a location 
    ~/myproject/manage.py collectstatic    
## allow port in firewall i installed 
    sudo ufw allow 8000
    
## start django server for testing
    ~/myproject/manage.py runserver 0.0.0.0:8000    
    
## check gunicorn django https server
    cd ~/myproject
    gunicorn --bind 0.0.0.0:8000 myproject.wsgi

## create service of gunicorn
working directory is where my manage.py file located
sproj.sock file should be located where my manage.py as well 
    
    sudo nano /etc/systemd/system/gunicorn.service
    

    [Unit]
    Description=Gunicorn service
    After=network.target
    
    [Service]
    User=clanzu2
    Group=www-data
    WorkingDirectory=/home/clanzu2/PycharmProjects/sproj
    ExecStart=/home/clanzu2/PycharmProjects/sproj/venv/bin/gunicorn --access-logfile - --workers 3 --bind unix:/home/clanzu2/PycharmProjects/sproj/sproj.sock sproj.wsgi:application
    
    [Install]
    WantedBy=multi-user.target
    ~                          

## start and enable gunicorn.service  (enable) so it ll start in boot

    sudo systemctl reload daemon 
    sudo systemctl start gunicorn
    sudo systemctl enable gunicorn
    sudo systemctl status gunicorn

## go to /etc/nginx/sites-availabe and create file sproj
    server {
        listen 80;
        server_name 0.0.0.0;
    
        location = /favicon.ico { access_log off; log_not_found off; }
        location /static/ {
            root /home/clanzu2/PycharmProjects/sproj;
        }
    
        location / {
            include proxy_params;
            proxy_pass http://unix:/home/clanzu2/PycharmProjects/sproj/sproj.sock;
        }
    }
    
## then enable the file to folder sites-enable
    sudo ln -s /etc/nginx/sites-available/sproj /etc/nginx/sites-enabled
    
## check nginx for mistakes 
    sudo nginx -t
## restart nginx 
    sudo systemctl restart nginx
    
## delete restrictions to connecct only 8000 port  and give full ports 
    sudo ufw delete allow 8000
    sudo ufw allow 'Nginx Full'            


    
    
                  
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    