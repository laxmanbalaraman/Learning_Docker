# Learning_Docker


A container is a software code package containing an application's code, its libraries, and other dependencies. Containerization makes your applications portable so that the same code can run on any device. A virtual machine is a digital copy of a physical machine.

An "image" is a lightweight, standalone, and executable package that contains everything needed to run a piece of software, including the code, runtime, system tools, libraries, and system dependencies.


**Choose base image wisely!**
never use LATEST in base image in dockerfile as since latest may vary in time, does can you enviroment become incompatible. So be specific in base images.

**Dockerfile**

 It contains a set of instructions and commands that specify how to create a Docker image, what should be included in the image, and how the image should be configured. 

exclude file in .dockerignore

by Defualt docker container gives us root access but this open more security vulnerablities. Hence always add a user access to containers.

Difference between RUN and CMD intstruction in dockerfile'
RUN: commands are executed when images is being built
CMD: command is executed when container is getting started

Dockerfile can have multiple RUN instruction but logically only one CMD instruction.

**Speeding up builds**

Docker images are build up in layers and each instruction in dockerfile can be considered a layer.
Docker reuses the layer if there is no change in that layer/instruction/files.
Once a layer is rebuil, all the following layers have to rebuilt.
So write instruction in such a way that unecessary building of layers in not happening
One such example is npm install, you do don't want to install node modules always when you modify application.
if any changes happens at upper layers of npm install, npm install get executed as well. :(
So write instructions in such a way that stable instructions are at top, volatile instructions are at bottom.

**Pruning**

Docker image pruning is a process that removes unused, dangling, or unnecessary images from your local Docker environment to free up disk space. Over time, as you work with Docker containers and images, you can accumulate a significant amount of data that may no longer be needed. Pruning helps to keep your system clean and prevent it from running out of storage space.

first prune containers and then prune images and some containers can use come dangling images so those images might not be pruned.

**Sharing images**

you can share images in [hub.docker.com](https://hub.docker.com)

when you push an images all the layers contained with the image are push, however if you push a modified image, only those modified layers and following layers are pushed, makeing the push process faster.