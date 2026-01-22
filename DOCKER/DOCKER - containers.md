side note : Virtual machines advancement to physical server, then containers are advancement to Virtual machines.

Docker add :  copy the files from specific URL and also Unzip the .tar .gz files automatically in the container but copy cannot
Docker copy : used only to copy files from host system into the container

CMD : the arguments that can be overridden is passed through CMD
Entry Point : the arguments that cannot be overridden is passed through entry point
![[container-what-is-container.png]]
**A container is a standard unit of software that packages up code and all its dependencies so the application runs quickly and reliably from one computing environment to another**. A Docker container image is a lightweight, standalone, executable package of software that includes everything needed to run an application: code, runtime, system tools, system libraries and settings.  
Container images become containers at runtime and in the case of Docker containers – images become containers when they run on [Docker Engine](https://www.docker.com/products/container-runtime). Available for both Linux and Windows-based applications, containerized software will always run the same, regardless of the infrastructure. Containers isolate software from its environment and ensure that it works uniformly despite differences for instance between development and staging.

Container has a minimal OS and it uses base OS of the server. 

![[Pasted image 20260113233010.png]]

Docker Engine ,is a SPOF => single point of failure
to overcome it ,we use **Buildah**

Podman : competitor of Docker, kind of more advance tools of the docker

## Architecture

client :
through docker daemon :  heart of docker , it is stops working ,docker fails
![[Pasted image 20260116042915.png]]

There are three important things,

1. docker build -> builds docker images from Dockerfile
2. docker run -> runs container from docker images
3. docker push -> push the container image to public/private regestries to share the docker images.
Docker file -> docker daemon -> docker image -> container

- reduces the heavy weight and increase efficiency by reducing manual work

Docker Hub is used for storing docker container and helps to share it with certain people
GitHub : is a source code storing platform
Docker Hub : stores docker images

Disadvantages :
- it has to be installed by root user only
- Daemon runs with root user
- Single spot of failure : if someone get access to root then system is compromised

to create and push the image to Docker Hub
docker build -> run -> push ( Docker Hub )

to run the image from Docker Hub
docker pull 
docker images -> to verify the files

