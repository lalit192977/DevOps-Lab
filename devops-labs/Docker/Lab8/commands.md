# Docker Lab 8 – Commands Reference

## List All Docker Networks

docker network ls

text

## Filter Out Bridge Driver

docker network ls | grep bridge

text

## Inspect Network Setting of a Container

docker inspect alpine-1 | grep Network

text

## Inspect the Default Bridge Network

docker network inspect bridge

text

## Run a Container With No Network

docker run -d --name alpine-2 --network none alpine

text

*(Corrected name: was written as "a;pine-2" earlier)*

## Create Custom Network with Subnet and Gateway

docker network create
--driver bridge
--subnet 182.18.0.0/24
--gateway 182.18.0.1
wp-mysql-network

text

## Run MySQL Container on Custom Network

docker run -d
--name mysql-db
--network wp-mysql-network
-e MYSQL_ROOT_PASSWORD=db_pass123
mysql:5.7

text

## Run Web App Linked to MySQL Over Same Network

docker run -d
--name mysql-app
--network wp-mysql-network
-p 38080:8080
--link mysql-db:mysql-db
-e DB_HOST=mysql-db
-e DB_Password=db_pass123
kodekloud/simple-webapp-mysql