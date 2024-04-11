`docker --version`

`docker login`

`docker pull [Image]` - pull image from docker hub

`docker search [image]` - search image in docker hub

`docker build -t [imagename] [dockerfile_path]` Build image from Dockerfile

`docker push <docker_username>/<docker_image_name>:<tag>` - push image to docker hub

`docker run -p [LOCALHOSTPORT]:[ContainerPORT] image:Release_Version` - run container 

`docker run -p [LOCALHOSTPORT]:[ContainerPORT] -e [envName]=[envValue] image:Release_Version` - run container with environment variables

`docker run -d -p [LOCALHOSTPORT]:[ContainerPORT] --name [nameForContainer] --network [networkName] image:Release_Version` - run container in detached mode

`docker run -v [volume/hostlocalpath]:[containerdatapath] [image]` - mount volume to container



`docker logs [ContainerIdOrName]` - display logs

`docker logs -f [ContainerIdOrName]` - full logs


`docker images` - show the list of docker images in system

`docker image history [ImageName]:[ReleaseVersion]`

`docker image history [imageId]` - show layers of image

`docker image inspect  [imageId]` - show details of image

`docker image remove [imageName/Id]` or `docker image remove [imageName]:[Releaseversion]` or `docker rmi [imageName]:[Releaseversion]`

`docker tag source_image:tag new_image:tag` - rename the docker image

`docker save -o image_name.tar image_name:tag` - save image to an tar archive

docker load -i image_name.tar - load image from an tar archive

docker image prune
----

`docker container ls` - show the list of running containers

`docker container ls -a` - show the list of all containers which are even exited

`docker container stop [ContainerName_or_Id]` - shutdown the container

`docker container start [ContainerName_or_Id]` - Start the stopped container

`docker container kill [ContainerName_or_Id]` - immediate kill

`docker container rm [ContainerName_or_Id]` - remove the container

`docker container pause  [ContainerName_or_Id]` - pause a running container

`docker container unpause [ContainerName_or_Id]`

`docker container inspect  [ContainerName_or_Id]`

`docker container stats [ContainerName_or_Id]`

`docker container prune` - delete all stopped containers

`docker logs container_name_or_id`
---


`docker system df`            #show disk usage of docker

`docker system events`                      # show all triggered events

`docker system prune -a`                    # delete all stopped containers & remove images which are not used

`docker stats [ContainerId]`

`docker exec -it [ContainerId] /bin/bash`

`docker exec -it [ContainerId] /bin/sh`

---
`docker network ls`                         # show the list of networks

`docker network inspect [networkName]` - Inspect details of a network

`docker network create [networkName]`  - Create a user-defined bridge network

`docker network prune`

`docker network rm [networkName]`
docker network connect network_name container_name - Connect a container to a network

docker network disconnect network_name container_name

---

`docker volume ls` - list all volumes

`docker volume prune`

`docker volume create`

`docker volume create [volumeName]` - create a named volume

`docker volume rm [VolumeName]` - remove volume

`docker volume inspect [volumeName]` - Inspect details of a volume


`docker cp local_file_or_directory container_name:/path/in/container` - Copy files between a container and a volume


---
`docker compose --version`

`docker compose up` - Create and start containers defined in a docker- compose.yml file

`docker compose up -d`  #detach mode

`docker compose up -d -build`  #Build Images before starting Containers

`docker compose up --scale [servicename]=[servicecount]`

`docker compose -f <filename> up`

`docker compose down`   # stop the containers & also remove the containers

`docker compose build`

`docker compose events`

`docker compose config`   # Show the configuration

`docker compose images`    # list the images used by compose

`docker compose ps`                # list down the containers

`docker compose top` #Display the running processes of a container

`docker compose pause`

`docker compose unpause`

`docker compose stop`

`docker compose logs` - view logs of services


`docker compose up -d --scale service_name=number_of_containers` - Scale services to a specific number of containers

`docker compose run service_name command` - run a one time command in service

---