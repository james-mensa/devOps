# Docker CLI Cheat Sheet

## Basic Docker Commands

| Command                  | Description                                       | Example                                    |
|--------------------------|---------------------------------------------------|--------------------------------------------|
| `docker run`             | Run a command in a new container                 | `docker run -d --name mycontainer ubuntu`  |
| `docker build`           | Build an image from a Dockerfile                 | `docker build -t myimage:latest .`         |
| `docker push`            | Push an image to a registry                      | `docker push myimage:latest`               |
| `docker pull`            | Pull an image from a registry                    | `docker pull ubuntu:latest`                |
| `docker stop`            | Stop a running container                         | `docker stop mycontainer`                  |
| `docker rm`              | Remove one or more containers                    | `docker rm mycontainer`                    |
| `docker ps`              | List running containers                          | `docker ps`                                |
| `docker ps -a`           | List all containers (including stopped ones)     | `docker ps -a`                             |
| `docker logs`            | Fetch logs from a container                      | `docker logs mycontainer`                  |
| `docker exec`            | Run a command in a running container             | `docker exec -it mycontainer bash`         |
| `docker attach`          | Attach to a running container’s stdin, stdout, and stderr | `docker attach mycontainer`            |
| `docker inspect`         | Return detailed information about a container or image | `docker inspect mycontainer`           |
| `docker network ls`      | List networks                                    | `docker network ls`                       |
| `docker volume ls`       | List volumes                                     | `docker volume ls`                        |
| `docker info`            | Display system-wide information                  | `docker info`                             |
| `docker version`         | Show Docker version information                  | `docker version`                          |
| `docker-compose up`      | Start up services defined in `docker-compose.yml` | `docker-compose up -d`                    |
| `docker-compose down`    | Stop and remove services defined in `docker-compose.yml` | `docker-compose down`              |
| `docker-compose logs`    | View logs from services defined in `docker-compose.yml` | `docker-compose logs`              |

## Advanced Docker Commands

| Command                  | Description                                       | Example                                    |
|--------------------------|---------------------------------------------------|--------------------------------------------|
| `docker run -d`          | Run a container in detached mode                  | `docker run -d --name mycontainer ubuntu`  |
| `docker run -p`          | Map container ports to host ports                 | `docker run -p 8080:80 nginx`              |
| `docker run -v`          | Mount a volume into the container                 | `docker run -v /host/path:/container/path myimage` |
| `docker build -t`        | Tag an image during build                         | `docker build -t myimage:1.0 .`            |
| `docker rmi`             | Remove one or more images                         | `docker rmi myimage`                       |
| `docker tag`             | Tag an image with a new name                      | `docker tag myimage myrepo/myimage:latest` |
| `docker system prune`    | Remove unused data (containers, networks, images) | `docker system prune -a`                   |
| `docker volume create`   | Create a new volume                               | `docker volume create myvolume`           |
| `docker network create`  | Create a new network                              | `docker network create mynetwork`         |

## Customization Tips

1. **Use Aliases:** For frequently used commands, create aliases in your shell configuration file (e.g., `.bashrc`, `.zshrc`) to simplify usage.
   ```bash
   alias dps='docker ps'
   alias dstop='docker stop'
