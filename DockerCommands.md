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

**Rename a container**
+ docker run --name new-name container-name

**detach a container**
docker run -d container-name

**View logs**
docker container log container-name<br/>
-f - follow logs, -n - last n logs 

**Execute a command in a running container**
+ docker exec -it 885960790fd6 bash

**Remove a container**
+ docker container rm container-name


**Push to docker hub repo**

Create a new repo in [hub.docker.com](https://hub.docker.com) and push the image from your local using repo-name:tagName

+ docker push laxmanbalaraman/test-repo:tagname

**publish port / port mapping**

+ docker run -d -p 8080:3000 --name container-alias-name image-name

**Persisting data in docker**

**Create a Volume**

+ docker volume create app-data

**Map app-data to a dir of contianer**

+ docker run -d -p 4000:3000 -v app-data:/app/data --name container-alias-name image-name 

**Copying files between host & container and vice-versa**

+ docker cp contianer-name:/path/to/file directory-path-to-save-file 
+ docker cp path-to-file contianer-name:/path/of/dir/

**Publishing source code to docker**

+ docker run -d -p 5001:3000 -v $(pwd):/app-folder image-name







