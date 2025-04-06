# What is Docker ?

Docker is an open-source platform that allows developers to automate the deployment, scaling, and management of applications using lightweight, portable containers. 

Containers package an application and its dependencies together, ensuring that it runs consistently across different environments, such as development, testing, and production.

# Where do images live

Container repository

Private Repositories

Public Repositories like DockerHub


# Commands

 > docker pull \<image\> (Dowloads latest image)

 > docker pull \<image\>:\<tag\> (Downloads image with tag , tag is similar to version)
 
 > docker images (list of images)

 > docker run \<image name\> (run docker image, creates a new container)

 > docker ps (List of running containers)

 > docker ps -a (all containers , running or stopped)

 > docker run -d \<image name\> (Run container in detached mode)

 > docker stop \<id of container\> (Stop the exisiting running container)

 > docker start \<id of container\> (Start the exiting stopped container by id)

 > docker logs \<ContainerID / Container name\>

# Binding local HOST to container PORT

> docker run -p\<HOST\>:\<PORT\> -d redis:6.2.17

**Example:**

> docker run -p6001:6379 -d redis:6.2.17

# Container with name

When we run a container , some dummy name is assigned to running container

To provide name we can add --name flag in command

docker run --name \<redis-server\> \<redis\>

# Access to terminal of running Container

> docker exec -it cd1b37d62174 /bin/bash


