# Portainer - Container management software for Docker and Kubernetes

## Installation

Create volume:

```sh
docker volume create portainer_data
```

Run the image for `linux container`:

```sh
docker run -d -p 8000:8000 -p 9443:9443 --name portainer --restart=always -v /var/run/docker.sock:/var/run/docker.sock -v portainer_data:/data portainer/portainer-ce:latest
```

Run the image for `windows container`:

```sh
docker run -d -p 8000:8000 -p 9443:9443 --name portainer --restart always -v \\.\pipe\docker_engine:\\.\pipe\docker_engine -v portainer_data:C:\data portainer/portainer-ce:latest
```

Lunch at [https://localhost:9443](https://localhost:9443)

Or use this docker compose:

```yaml

volumes:
  portainer-data:
    driver: local
services:
  app:
    container_name: portainer
    image: portainer/portainer-ce:latest
    ports:
      - 9000:9000
      - 9443:9443
      - 8000:8000
    volumes:
      - /var/run/docker.sock:/var/run/docker.sock
      - portainer-data:/data
    restart: unless-stopped

```
