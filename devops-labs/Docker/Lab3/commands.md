```bash

docker ps
docker exec eloquent_goldwasser printenv
docker exec eloquent_goldwasser printenv APP_COLOR

 docker run -d --name blue-app -e APP_COLOR=blue -p 38282:8080 kodekloud/simple-webapp

docker run -d --name mysql-db -e MYSQL_ROOT_PASSWORD=db_pass123 mysql  














## commands.md Content

```markdown
# Docker Lab 3 - Commands Reference

## Container Management Commands

### List Running Containers
```bash
# Display all running containers with details
docker ps


Docker Lab 3 - GitHub Repository Structure
Recommended Directory Structure
