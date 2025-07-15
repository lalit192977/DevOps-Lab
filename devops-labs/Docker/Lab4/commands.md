# Docker Lab 4 – Commands Reference

## 1. Count Images

docker images -q | wc -l

text

## 2. List Images with Filters

docker images ubuntu
docker images nginx

text

## 3. Build and Explore Custom Image

cd webapp-color
ls
cat Dockerfile
docker build -t webapp-color .

text

## 4. Run and Manage Containers

docker run -d --name webb -p 8282:8080 webapp-color
docker stop webb

text

## 5. Test and Inspect with Python Image

docker run -it python:3.6 cat /etc/os-release

text

## 6. List New Images

docker images webapp-color

text

## 7. Multi-Tag/Multi-Variant Images

vi Dockerfile # Edit or inspect Dockerfile for modifications
docker build -t webapp-color-slim .
docker images webapp-color-slim

text

## 8. Run ‘lite’ Variant of Webapp

docker run -d -p 8383:8080 webapp-color:lite