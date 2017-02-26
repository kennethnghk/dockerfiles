# dockerfiles

Docker files for different applications

## Basic docker commands

* Build image from dockerfile 

```
docker build -t <repository>/<tag> .
```

* View all containers

```
docker ps
```

* View all images

```
docker images
```

* Run into a new container 

```
docker run --name <container name> -it <image>
```

The `-it` instructs Docker to allocate a pseudo-TTY connected to the container’s stdin; creating an interactive bash shell in the container. 
