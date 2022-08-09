
[python](https://runestone.academy/runestone/books/published/pythonds/index.html)
[docker](https://testdriven.io/blog/dockerizing-django-with-postgres-gunicorn-and-nginx/)
[docker to kubernets](appdynamics.com/blog/product/migrating-from-docker-compose-to-kubernetes/#:~:text=One%20difference%20to%20note%20is,be%20added%20or%20removed%20dynamically.&text=With%20Kubernetes%2C%20we%20would%20have,a%20structure%20called%20a%20DaemonSet.)
[docker-compose install](https://docs.docker.com/compose/install/)
[docker install](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-18-04)
[docker for ubuntu 22](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-20-04)

[docker for windows](https://futurestud.io/tutorials/how-to-fix-exec-user-process-caused-no-such-file-or-directory-in-docker)

[dump postgres](https://devopsheaven.com/postgresql/pg_dump/databases/docker/backup/2017/09/10/backup-postgresql-database-using-docker.html)

[dokcer cache](https://pythonspeed.com/articles/docker-cache-pip-downloads/)
## to start docker in windows convert file format from dos to unix with dos2unix _yourfile.sh_

## install docker

        sudo apt install docker

## install docker-compose

        pip install docker-compose

## edit .bashrc

        vim ~/.bashrc

        which docker-compose

        export something="pathto docker-compose"

## list images of docker

        sudo docker images -a

## list id of images of docker

        sudo  images -qa

## delete image of docker

        sudo docker rmi "id"

## delete all images of docker

        sudo docker rmi $(sudo docker images -qa)


## Delete all volumes
        docker volume rm $(docker volume ls -q)


## list containers of docker

        sudo docker ps -a

## list only id of container

        sudo  ps -aq

## remove special container

        sudo docker rm "id"

## remove all containers

        sudo docker rm $(sudo docker ps -qa)

## create network for docker
        docker network create -d bridge my-bridge-network

## remove all docker network interfaces

        sudo docker inspect 1d55bb8b35c6

        sudo docker network rm $(docker network ls -q)

## list docker network interfaces

        sudo docker network rm $(sudo docker network ls -q)

## build container

        sudo dokcer build -t "name of container" .

## run built container

        sudo docker run --name "image name" -d "name of container"

## outside folder mount to docker

        sudo docker run --rm --name web -p 8080:8080 -v /home/clanzu2/dockerTest/resources:/usr/c/app/resources web

## docker-compose to start django project

        docker-compose run app sh -c "django-admin.py startproject app ."

## in case of error for logs

        docker-compose -f docker-compose.prod.yml logs -f

## to see docker container logs
        sudo docker logs container_id -f 

## to turn down dev container

        sudo docker-compose down -v

## to run dev container

       sudo docker-compose up -d --build

## run dev migrations

        docker-compose exec web python manage.py migrate --noinput

## run production docker

        sudo docker-compose down -v
        sudo docker-compose -f docker-compose.prod.yml up -d --build
        sudo docker-compose -f docker-compose.prod.yml exec web python manage.py migrate --noinput
        sudo docker-compose -f docker-compose.prod.yml exec web python manage.py collectstatic --no-input --clear

        sudo docker-compose -f docker-compose.prod.yml up -d --force-recreate --no-deps --build nginx

        [important to create and run container](https://docs.docker.com/compose/reference/up/)

## to be able to use Pillow in django in docker install Pillow dependencies

        RUN apk add zlib libjpeg-turbo-dev libpng-dev freetype-dev lcms2-dev libwebp-dev \
        harfbuzz-dev fribidi-dev tcl-dev tk-dev


## to connect to running docker container if alpine

        sudo docker exec -it "container_name" sh

## to connect to running docker container if any other image like ubuntu or centos
        
        sudo docker exec -it "containter_name" bash


## to connect to datebase 

        docker-compose exec db psql --username=hello_django --dbname=hello_django_dev


## to install pgadmin4 (apt)[https://www.pgadmin.org/download/pgadmin-4-apt/]