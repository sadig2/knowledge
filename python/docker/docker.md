## list images of docker
        sudo docker images -a
## list id of images of docker
        sudo docker images -qa
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
## build container
        sudo dokcer build -t "name of container" .
## run built container
        sudo docker run --name "image name" -d "name of container"
## outside folder mount to docker
        sudo docker run --rm --name web -p 8080:8080 -v /home/clanzu2/dockerTest/resources:/usr/c/app/resources web
