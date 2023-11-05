# Learning_Docker


A container is a software code package containing an application's code, its libraries, and other dependencies. Containerization makes your applications portable so that the same code can run on any device. A virtual machine is a digital copy of a physical machine.

An "image" is a lightweight, standalone, and executable package that contains everything needed to run a piece of software, including the code, runtime, system tools, libraries, and system dependencies.


**Choose base image wisely!**
never use LATEST in base image in dockerfile as since latest may vary in time, does can you enviroment become incompatible. So be specific in base images.

