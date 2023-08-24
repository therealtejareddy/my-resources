`docker --version`

`docker login`

`docker pull [Image]`

`docker search [image]`

`docker push <docker_username>/<docker_image_name>`

`docker run -p [LOCALHOSTPORT]:[ContainerPORT] image:Release_Version`

`docker run -p [LOCALHOSTPORT]:[ContainerPORT] -e [envName]=[envValue] image:Release_Version`

`docker run -d -p [LOCALHOSTPORT]:[ContainerPORT] --name [nameForContainer] --network [networkName] image:Release_Version` # run container in detached mode

`docker run -v [volume/hostlocalpath]:[containerdatapath] [image]`

``

> -p == --publish, -d=detachmode, --name = with this tag we can assign own name to container & it should be unique

`docker logs [ContainerId]`

`docker logs -f [ContainerId]`

==> -f==full

`docker images` # show the list of docker images in system

`docker image history [ImageName]:[ReleaseVersion]`

`docker image history [imageId]`            #show layers of image

`docker image inspect  [imageId]`          #show details of image

`docker image remove [imageName/Id]`

`docker image remove [imageName]:[Releaseversion]`

----

`docker container ls`          # show the list of running containers

`docker container ls -a`         # show the list of all containers which are even exited

`docker container stop [ContainerId]`            #shutdown the container

`docker container start [ContainerId]`           # Start the stopped container

`docker container kill [ContainerId]`           #immediate kill

`docker container rm [ContainerId]`

`docker container pause  [ContainerId]`

`docker container unpause [ContainerId]`

`docker container inspect  [ContainerId]`

`docker container stats [ContainerId]`

`docker container prune`              # delete all stopped containers

---


`docker system df`            #show disk usage of docker

`docker system events`                      # show all triggered events

`docker system prune -a`                    # delete all stopped containers & remove images which are not used

`docker stats [ContainerId]`

`docker exec -it [ContainerId] /bin/bash`

`docker exec -it [ContainerId] /bin/sh`

---
`docker network ls`                         # show the list of networks

`docker network inspect [networkName]`

`docker network create [networkName]` 

`docker network prune`

`docker network rm [networkName]`

---

`docker volume ls`

`docker volume prune`

`docker volume create`

`docker volume create [volumeName]`

`docker volume rm [VolumeName]`

`docker volume inspect [volumeName]`

---
`docker compose --version`

`docker compose up`

`docker compose up -d`  #detach mode

`docker compose up -d -build`  #Build Images before starting Containers

`docker compose up --scale [servicename]=[servicecount]`

`docker compose -f <filename> up`

`docker compose down`   # stop the containers & also remove the containers

`docker compose events`

`docker compose config`   # Show the configuration

`docker compose images`    # list the images used by compose

`docker compose ps                # list down the containers

`docker compose top` #Display the running processes of a container

`docker compose pause`

`docker compose unpause`

`docker compose stop`

`docker compose logs`

---