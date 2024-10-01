
# Docker Command Guide

This document provides an overview of the most common Docker commands, including descriptions and parameters.

## 1. `docker --version`

Checks the installed version of Docker.

### Parameters:
- **N/A**: This command has no parameters.

### Example:
```bash
docker --version
```

---

## 2. `docker pull <image>`

Downloads an image from Docker Hub or a specific repository.

### Parameters:
- `<image>`: The name of the image you want to download (e.g., `ubuntu`, `nginx`).

### Example:
```bash
docker pull ubuntu
```

---

## 3. `docker images`

Lists all images available locally.

### Parameters:
- **N/A**: This command has no parameters.

### Example:
```bash
docker images
```

---

## 4. `docker rmi <image>`

Removes a local image.

### Parameters:
- `<image>`: The name or ID of the image you want to remove.

### Example:
```bash
docker rmi ubuntu
```

---

## 5. `docker run <options> <image>`

Runs a container from an image.

### Parameters:
- `<options>`: Additional options (see the list below).
  - `-d`: Runs the container in detached mode (in the background).
  - `--name <name>`: Assigns a name to the container.
  - `-p <host_port>:<container_port>`: Maps the host port to the container port.
  - `-v <host_dir>:<container_dir>`: Mounts a directory from the host into the container.

- `<image>`: The name of the image you want to run.

### Example:
```bash
docker run -d --name my_nginx -p 8080:80 nginx
```

---

## 6. `docker ps`

Lists the running containers.

### Parameters:
- **-a**: Lists all containers, including stopped ones.

### Example:
```bash
docker ps
```
```bash
docker ps -a
```

---

## 7. `docker stop <container_id>`

Stops a running container.

### Parameters:
- `<container_id>`: The ID or name of the container you want to stop.

### Example:
```bash
docker stop my_nginx
```

---

## 8. `docker start <container_id>`

Starts a stopped container.

### Parameters:
- `<container_id>`: The ID or name of the container you want to start.

### Example:
```bash
docker start my_nginx
```

---

## 9. `docker rm <container_id>`

Removes a container.

### Parameters:
- `<container_id>`: The ID or name of the container you want to remove.

### Example:
```bash
docker rm my_nginx
```

---

## 10. `docker exec <options> <container_id> <command>`

Executes a command in a running container.

### Parameters:
- `<options>`: Additional options (see the list below).
  - `-it`: Allows interaction with the terminal.
  
- `<container_id>`: The ID or name of the container in which you want to execute the command.
- `<command>`: The command you want to run inside the container.

### Example:
```bash
docker exec -it my_nginx /bin/bash
```

---

## 11. `docker logs <container_id>`

Displays the logs of a container.

### Parameters:
- `<container_id>`: The ID or name of the container whose logs you want to view.

### Example:
```bash
docker logs my_nginx
```

---

## 12. `docker-compose up`

Starts the services defined in the `docker-compose.yml` file.

### Parameters:
- `-d`: Runs the services in detached mode.
  
### Example:
```bash
docker-compose up -d
```

---

## 13. `docker-compose down`

Stops and removes all containers, networks, and volumes defined in the `docker-compose.yml` file.

### Parameters:
- **N/A**: This command has no parameters.

### Example:
```bash
docker-compose down
```

---

## Conclusion

This guide provides a basic overview of Docker commands. For more information, refer to the [official Docker documentation](https://docs.docker.com/).
