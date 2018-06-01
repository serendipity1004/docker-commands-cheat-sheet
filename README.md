# docker-commands-cheat-sheet

## Container

```sh
# Run Container
docker container run <image>
  -it         : Bind STDIO
  -e          : Environment variable e.g. ENV=ENV
  -p          : Specify Port e.g. 5000:5000 (image:local)
  --net       : Name of the network e.g. redvelvetnetwork
  --name      : Specify name of the image e.g. redvelvetimage
  --rm        : Remove if same container exists
  -d          : Run container in background and detach
  -v          : Mount Directory e.g. $PWD:/app (local:docker)
  
# View Logs of Containers
docker container logs <container>
  -f          : Real time feedback
  --restart   : options ['on-failure']
  
# Container Metrics
docker container stats

# Execute Commands
docker container exec
  -it         : Same as run
  --user      : Run command as <user> e.g. seulki, "$(id -u):$(id -g)"
```

## Image

```sh
# List Images
docker image ls
  -a          : Also show deleted ones
  
# Delete Images
docker image rm

# Build Image
docker image build <image>
  -t        : Tag e.g. redvelvetimage
```

## Pull

```sh
# Pull Images From Docker Hub
docker pull <image>
```

## Network

```sh
# View Networks
docker network ls

# Create Networks
docker network create 
  --driver   : Driver to manage network
```

## Volume

```sh
# Create Volume
docker volume create <volume-name>

# Inspect Volume
docker volume inspect <volume-name>
```

## System
```sh
# See Overview
docker system df
  -v        : Verbose
  
# Docker Info
docker system info

# Clean Up Images
docker system prune
```
