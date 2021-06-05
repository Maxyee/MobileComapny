# Docker with Nodejs

All of the learning materials and docker command list is written with my own work so that I can work easily with docker

## How to check docker is running or not.

`sudo systemctl status docker`

## How to enable or disable the docker container

`sudo systemctl enable --now docker`

## Find all the docker images from the local machine

`sudo docker images`

## Find the docker container

`sudo docker ps`

or

`sudo docker container ls`

## How to pull docker registry images

visit this website: https://hub.docker.com/

## Running a container

`sudo docker run -d imagename:tagname`

## Exposing port in docker

`sudo docker run -d -p port-I-want:container-port imagename:tagname`

## How to stop a specific container in docker

`sudo docker stop CONTAINERID`

## Exposing Multiple port in docker

`sudo docker run -d -p portIwant:container-port -p anotherPortIWant:container-port imagename:tagname`
