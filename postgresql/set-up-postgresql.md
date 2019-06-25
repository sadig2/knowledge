## install postgres for ubuntu 

    sudo apt install postgresql postgresql-contrib
    


## edit /var/lib/pgsql/data/pg_hba.conf     set modes from ident ->trust
## for ubuntu go to /etc/postgresql/10/main  to configure pg_hba.conf
systemctl enable postgresql.service    it ll generate folders in /var/lib/pgsql/data  

## delete database 
    DROP USER [ IF EXISTS ] name [, ...]




## to switch to postgres user of server
    sudo -i -u postgres  

    \password     
    
    use “databasenam”;  
    
    \du - list users
    \l - list databases 
    \?   - help  
    \dp -  list tables  
    \dt - list tables  
    
    \d “tablename”    - shows table content  
    
## switch to specific user and database 
    psql "db" "user"    


## delete user 
    drop user "username";
## delete database 
    drop database "dbname";

    
    CREATE TABLE table_name(  
        id SERIAL  
    );  
    is equivalent to the following statements:  
    
    CREATE SEQUENCE table_name_id_seq;  
     
    CREATE TABLE table_name (  
        id integer NOT NULL DEFAULT nextval('table_name_id_seq')  
    );  
     
    ALTER SEQUENCE table_name_id_seq  
    OWNED BY table_name.id;  




postgres=# CREATE USER sadig WITH PASSWORD '1122' CREATEDB;     

CREATE DATABASE mydatabase;  

GRANT ALL PRIVILEGES ON DATABASE mydatabase TO clanzu;   

psql mydatabase clanzu  чтобы подключиться к базе данных 

ALTER USER clanzu WITH ENCRYPTED PASSWORD '1122';  

edit /var/lib/pgsql/data/pg_hba.conf     set modes from ident -> md5 or whatever u like  




CREATE TABLE account(  
user_id serial PRIMARY KEY,  
username VARCHAR (50) UNIQUE NOT NULL,  
password VARCHAR (50) NOT NULL,  
email VARCHAR (355) UNIQUE NOT NULL,  
created_on TIMESTAMP NOT NULL,  
last_login TIMESTAMP  
);  




pg_dump -U sadig mydatabase > gdfd.sql 


