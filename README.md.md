
# Docker and Docker-Compose Commands Cheat Sheet

## Docker Commands

### General
- `docker --version` : Check Docker version
- `docker info` : Display system-wide information

### Container Management
- `docker ps` : List running containers
- `docker ps -a` : List all containers (running and stopped)
- `docker run <image>` : Run a container from an image - <image> image id or image-name
- `docker run -d <image>` : Run container in detached mode - <image> image id or image-name
- `docker run -it <image> /bin/bash` : Run container interactively with a bash shell - <image> image id or image-name
- `docker stop <container_id>` : Stop a running container - <container_id> container id or container-name
- `docker start <container_id>` : Start a stopped container - <container_id> container id or container-name
- `docker restart <container_id>` : Restart a container - <container_id> container id or container-name
- `docker rm <container_id>` : Remove a container - <container_id> container id or container-name
- `docker rm $(docker ps -a -q)` : Remove all containers

### Image Management
- `docker images` : List images
- `docker pull <image>` : Pull image from Docker Hub - <image> image name:tag
- `docker build -t <tag> .` : Build image from Dockerfile in current directory
- `docker rmi <image_id>` : Remove an image
- `docker rmi $(docker images -q)` : Remove all images

### Logs and Inspect
- `docker logs <container_id>` : Show logs of a container
- `docker exec -it <container_id> /bin/bash` : Execute bash shell inside running container
- `docker inspect <container_id>` : Show low-level information on a container or image

### Volumes and Networks
- `docker volume ls` : List volumes
- `docker volume create <volume_name>` : Create a volume
- `docker volume rm <volume_name>` : Remove a volume
- `docker network ls` : List networks
- `docker network create <network_name>` : Create a network
- `docker network rm <network_name>` : Remove a network

---

## Docker-Compose Commands

- `docker-compose --version` : Check docker-compose version
- `docker-compose up` : Create and start containers defined in docker-compose.yml
- `docker-compose up -d` : Start containers in detached mode
- `docker-compose down` : Stop and remove containers, networks, images created by up
- `docker-compose ps` : List containers started by docker-compose
- `docker-compose logs` : View output from containers
- `docker-compose build` : Build or rebuild services
- `docker-compose stop` : Stop running containers without removing them
- `docker-compose restart` : Restart services
- `docker-compose exec <service> <command>` : Execute a command inside a running container

---

## Useful Tips

- Use `docker system prune` to remove unused data (containers, images, networks, volumes)
- Use `docker-compose config` to validate and view the compose file

---

*Keep this cheat sheet handy for quick reference!*
