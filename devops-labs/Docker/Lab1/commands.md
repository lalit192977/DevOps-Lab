## Docker Version
```bash
docker version

docker info

docker run -d --name nginx-1 nginx

docker ps -1 | wc -l
docker ps

docker images
docker images -q | wc -l

docker run -d --name rediss redis

docker stop rediss

docker ps -q | wc -l

docker ps -aq | wc -l

docker ps -a --filter ancestor=alpine --filter status=exited

docker ps -a --filter ancestor=alpine

docker rm -f $(docker ps -aq)

docker rmi ubuntu

docker pull nginx:1.14-alpine

docker run -d --name webapp nginx:1.14-alpine

docker rmi -f $(docker images -q)
