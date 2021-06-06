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
or
`sudo docker stop NAMES`

## Exposing Multiple port in docker

`sudo docker run -d -p portIwant:container-port -p anotherPortIWant:container-port imagename:tagname`

## All the docker container list history

`sudo docker ps -a`

## How to delete a container

`sudo docker rm ContainerID`

## How to find all the container id list

`sudo docker ps -aq`

## How to delete all the stopped container

`sudo docker rm $(docker ps -aq)`

## How to delete all container either running or stopped

`sudo docker rm -f $(docker ps -aq)`

## How to set a docker container name when It is about to run

`sudo docker run --name giveThename -d -p port-I-want:container-port imagename:tagname`

## How to share volums between Host and Container in docker
