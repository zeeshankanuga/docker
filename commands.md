# Docker Commands

Some of the most commonly used docker commands are 

### Lists docker images on the host machine.
```
docker images
```
### Builds image from Dockerfile.
```
docker build
```
### Runs a Docker container. 
```
docker run
```
 

There are many arguments which you can pass to this command for example,

- `docker run -d` -> Run container in background and print container ID
- `docker run -p` -> Port mapping

use `docker run --help` to look into more arguments.

### Lists running containers on the host machine.
```
docker ps
```


### Stops running container.
```
docker stop
```


### Starts a stopped container.
```
docker start
```

### Removes a stopped container.
```
docker rm
```

### Removes an image from the host machine.
```
docker rmi
```

### Downloads an image from the configured registry.
```
docker pull
```

### Uploads an image to the configured registry.
```
docker push
```

### Run a command in a running container.
```
docker exec
```

### Manage Docker networks such as creating and removing networks, and connecting containers to networks. 
```
docker network
```
