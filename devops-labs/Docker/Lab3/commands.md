```bash

docker ps
docker exec eloquent_goldwasser printenv
docker exec eloquent_goldwasser printenv APP_COLOR

 docker run -d --name blue-app -e APP_COLOR=blue -p 38282:8080 kodekloud/simple-webapp

docker run -d --name mysql-db -e MYSQL_ROOT_PASSWORD=db_pass123 mysql  