[docker](https://testdriven.io/blog/dockerizing-django-with-postgres-gunicorn-and-nginx/)
[docker-compose install](https://linuxize.com/post/how-to-install-and-use-docker-compose-on-ubuntu-18-04/)

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

## list containers of docker

        sudo docker ps -a

## list only id of container

        sudo docker ps -aq

## remove special container

        sudo docker rm "id"

## remove all containers

        sudo docker rm $(sudo docker ps -qa)

## remove all docker network interfaces

        sudo docker network rm $(docker network ls -q)

## list docker network interfaces

        sudo docker network rm $(docker network ls -q)

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

## to turn down dev container

        sudo docker-compose down -v

## to run dev container

       sudo docker-compose up -d --build

## run dev migrations

        docker-compose exec web python manage.py migrate --noinput

## run production docker

        docker-compose down -v
        docker-compose -f docker-compose.prod.yml up -d --build
        docker-compose -f docker-compose.prod.yml exec web python manage.py migrate --noinput
        docker-compose -f docker-compose.prod.yml exec web python manage.py collectstatic --no-input --clear

## to be able to use Pillow in django in docker install Pillow dependencies

        RUN apk add zlib libjpeg-turbo-dev libpng-dev freetype-dev lcms2-dev libwebp-dev \
        harfbuzz-dev fribidi-dev tcl-dev tk-dev
