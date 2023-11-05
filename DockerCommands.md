# Docker Commands


### Images

list all images

+ docker images
+ docker image ls

### Containers

show running containers
+ docker ps

show also stopped container
+ docker ps -a

start a container
+ docker start container-name

stop a container
+ docker stop container-name


Create and run a new container from an image
+ docker run -it image-name
(use this when create a new image and interact with in immediately)

Execute a command in a running container
+ docker exec -it 885960790fd6 bash





