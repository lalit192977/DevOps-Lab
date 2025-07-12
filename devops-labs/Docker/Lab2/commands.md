```bash

docker ps -q | wc -l

docker ps 
docker inspect mystifying_snyder --format '{{.Config.Image}}'

docker ps
docker inspect 5b62edc4f16b --format '{{.NetworkSettings.Ports}}'
docker port 5b62edc4f16b

docker port 5b62edc4f16b

docker run -d --name blue-app -p 38282:8080 kodekloud/simple-webapp:blue





```



```markdown
# Docker Lab 2 - Commands Reference

## Container Management Commands

### Count Running Containers
```bash
# Count all running containers
docker ps -q | wc -l
List Container Information
