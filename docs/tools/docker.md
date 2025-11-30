# Docker Cheat Sheet

Docker allows you to package applications into containers.

## Basic Commands

| Command | Description |
| :--- | :--- |
| `docker run <image>` | Run a container from an image |
| `docker ps` | List running containers |
| `docker ps -a` | List all containers (including stopped) |
| `docker images` | List available images |
| `docker stop <id>` | Stop a running container |
| `docker rm <id>` | Remove a container |
| `docker rmi <image>` | Remove an image |

## Building Images

Create a `Dockerfile`:

```dockerfile
FROM python:3.9-slim
WORKDIR /app
COPY . .
CMD ["python", "app.py"]
```

Build the image:

```bash
docker build -t my-app:v1 .
```

## Running Containers

```bash
# Run in background (-d) and map port (-p host:container)
docker run -d -p 8080:80 my-app:v1
```