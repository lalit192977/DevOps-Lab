# Docker Lab 9 – All Commands Used

## Step 1: Run a Docker Local Registry

docker run -d
--name my-registry
-p 5000:5000
--restart always
registry:2

text

## Step 2: Check Registry Status

docker ps -a | grep 5000
docker ps -a --filter "publish=5000"

text

## Step 3: Check Port Usage

sudo lsof -i :5000
sudo netstat -tuln | grep 5000
sudo ss -ltnp | grep :5000

text

## Step 4: Pull Latest Images

docker pull nginx:latest
docker pull httpd:latest

text

## Step 5: Tag Images for Localhost Registry

docker tag nginx:latest localhost:5000/nginx
docker tag httpd:latest localhost:5000/httpd

text

## Step 6: Push Images to Localhost Registry

docker push localhost:5000/nginx
docker push localhost:5000/httpd

text

## Step 7: Remove Registry and Cleanup

docker rm -f my-registry
docker image prune -a
docker images

text

## Step 8: Re-run Registry on Port 5050 (If Port Conflict)

docker run -d
--name my-registry
-p 5050:5000
--restart always
registry:2

text

## Alternate Port Tags

docker tag nginx:latest localhost:5050/nginx
docker tag httpd:latest localhost:5050/httpd

docker push localhost:5050/nginx
docker push localhost:5050/httpd