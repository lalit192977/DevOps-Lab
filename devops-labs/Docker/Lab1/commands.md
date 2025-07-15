# Docker Commands – Lab 1

## System Info

docker version
docker info

text

## Run and Interact with Containers

docker run -d --name nginx-1 nginx
docker ps -1 | wc -l
docker ps

text

## Images and Containers

docker images
docker images -q | wc -l

docker run -d --name rediss redis
docker stop rediss

docker ps -q | wc -l
docker ps -aq | wc -l

text

## Filtering Containers by Image

docker ps -a --filter ancestor=alpine --filter status=exited
docker ps -a --filter ancestor=alpine

text

## Cleanup

docker rm -f $(docker ps -aq)
docker rmi ubuntu

text

## Pull Specific Version and Deploy

docker pull nginx:1.14-alpine
docker run -d --name webapp nginx:1.14-alpine

docker rmi -f $(docker images -q)

# Docker Lab 1 – Task Breakdown

---

## Task 1: Check Docker Version and Info

docker version
docker info

text
📸 Screenshot: `01_docker_version.png`

---

## Task 2: Deploy NGINX in Detached Mode

docker run -d --name nginx-1 nginx

text
📸 Screenshot: `02_run_nginx.png`

---

## Task 3: Count & List Running Containers

docker ps -1 | wc -l
docker ps

text
📸 Screenshot: `03_list_containers.png`

---

## Task 4: Deploy & Stop Redis

docker run -d --name rediss redis
docker stop rediss

text
📸 Screenshots: `04_run_redis.png`, `05_stop_redis.png`

---

## Task 5: Use Filters for Alpine-Based Containers

docker ps -a --filter ancestor=alpine --filter status=exited
docker ps -a --filter ancestor=alpine

text
📸 Screenshot: `06_filter_alpine.png`

---

## Task 6: Remove All Containers and Images

docker rm -f $(docker ps -aq)
docker rmi ubuntu
docker rmi -f $(docker images -q)

text
📸 Screenshot: `07_remove_all_objects.png`

---

## Task 7: Pull Specific Image and Run WebApp

docker pull nginx:1.14-alpine
docker run -d --name webapp nginx:1.14-alpine

text
📸 Screenshot: `08_deploy_webapp_nginx.png`