# dockerfiles

Docker files for different applications

## Basic docker commands

* Build image from dockerfile 

```
docker build -t <repository>/<tag> .
```

`-f` : Name of dockerfile

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

`-it` : Instructs Docker to allocate a pseudo-TTY connected to the container’s stdin; creating an interactive bash shell in the container. 

`-d` : Run in detached (background) mode

* Stop container

```
docker stop <container>
```

## Dockerfile

* `ENTRYPOINT`
An ENTRYPOINT allows you to configure a container that will run as an executable.
