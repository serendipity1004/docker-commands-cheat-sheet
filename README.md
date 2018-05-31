# docker-commands-cheat-sheet

## Container

```sh
# Run Container
docker container run <image>
  -it         : Bind STDIO
  -e          : Environment variable e.g. ENV=ENV
  -p          : Specify Port e.g. 5000:5000 (image:local)
  --name      : Specify name of the image e.g. redvelvetimage
  --rm        : Remove if same container exists
  -d          : Run container in background and detach
  
# View Logs of Containers
docker container logs <container>
  -f          : Real time feedback
  --restart   : options ['on-failure']
  
# Container Metrics
docker container stats
```

## Image

```sh
# List Images
docker image ls
  -a          : Also show deleted ones
  
# Delete Images
docker image rm
```
