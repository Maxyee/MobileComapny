# Docker with Database

All of the learning materials and docker command list is written with my own style so that I can work easily with docker

## How to make a mysql with mysql-server5.7 image using docker

`sudo docker run -p 3307:3306 --name my-mysql -e MYSQL_ROOT_PASSWORD=root -d mysql/mysql-server:5.7`

## How to execute mysql inside the docker machine

`sudo docker exec -it my-mysql /bin/bash`

## How to excess docker mysql from local machine

`mysql -uroot -p -A`

`select user,host from mysql.user;`

`update mysql.user set host='%' where user='root';`

`flush privileges;`

`mysql -uroot -p -P3307 -h127.0.0.1`

### Local machine mysql

1. At first install the mysql
   `sudo apt update`
   `sudo apt upgrade`
   `sudo apt install mysql-server`
   `mysql --version`
2. set the root password
   `sudo mysql_secure_installation`

3. if we set root user password then we have to run this command when starting mysql locally

`sudo mysql -u root -p`

4. if we dont set password then we have run this command

`sudo mysql -u root`

5. after connecting the mysql we can use some mysql command

`show databases;`
`use yourdatabase;`
`show tables`

6. finally we can also use the mysql workbench

## How to check docker is running or not.

`sudo systemctl status docker`

## How to enable or disable the docker

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
