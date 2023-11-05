# Docker Commands


### Images

**list all images**

+ docker images
+ docker image ls

**Build an image from dockerfile**
+ docker build -t image-name path-dockerfile

**Prune images**
+ docker image prune

**Remove image**
+ docker image rm image-name

**Tagging images**

tagging at build <br/>
+ docker build -t image-tag-name <br/>
+ docker tag SOURCE_IMAGE[:TAG] TARGET_IMAGE[:TAG]

**Deleta a tag**
+ docker image remove image-name[:TAG]

**Saving and Loading images**
+ docker image save image-name
+ docker image load -i image-tar-file


### Containers

**show running containers**
+ docker ps

**show also stopped container**
+ docker ps -a

**start a container**
+ docker start container-name

**stop a container**
+ docker stop container-name

**Prune containers**
+ docker container prune

**Create and run a new container from an image**
+ docker run -it image-name
(use this when create a new image and interact with in immediately)

**Execute a command in a running container**
+ docker exec -it 885960790fd6 bash


**Push to docker hub repo**

Create a new repo in [hub.docker.com](https://hub.docker.com) and push the image from your local using repo-name:tagName

docker push laxmanbalaraman/test-repo:tagname






