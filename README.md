# learning-docker
learning docker new course from linkedin learning


## starting docker container in longer way

**create conainer hello-worlds like this** </br>

```dj
docker container create hello-world:linux
```

**see running containers** </br>
```dj 
docker ps 
```

**see all the containers created** </br>
```dj
docker ps --all
```
**start container by their id** </br>
```dj
docker container start then_docker_long_id
```

**see the docker log** </br>
```dj
docker logs then_docker_id_or_part_of_the_id
```

**start container by their id in attached mode** </br>
```dj
docker container start --attach then_docker_long_id
```



## create docker container in short way

**just use run for creating docker container and use linux for** </br>

```dj
docker run hello-world:linux
```

docker run =
docker container create
(+) docker container start
(+) docker container attach

## create docker container from Dockerfile

**first use build then the name of the container that you want to give after that Dockerfile name, if your not using the default file name which is Dockerfile** </br>

```dj
docker build -t container_name . or /path/to/some where
docker build -t container_name -f or --file Dockerfile_name_if_notusing_the_default_name
```

**then run the container**</br>

```dj
docker run name_of_the_container
```


**using another build with serverdocker file this time slight chnage in command**</br>

```dj
docker build --file server.Dockerfile --tag name_of_container .
```

**don't use docker run container_name when the container is server or never stops
otherwise it will hang** </br>

**then you need to open another terminal find the docker id
and kill it like this** </br>
```dj
docker ps
docker kill container_docker_id
```

**you can type this instead it will run in background**</br>
```dj
docker run -d your_server
```

**docker exec kind of inspect the container** </br>
**if you want to know the date of container**</br>
```dj
docker exec container_id date
```

**if you want a interactive bash shell for the container like
we don in postgres use the following command** </br>

**to exit out of the interactive terminal press ctr + d** </br>

```dj
docker exec --interactive --tty container_id bash
```


**stop unnessesary docker through stop command that takes times little bit** </br>
```dj
docker stop docker_id
```

**to stop forcefully and faster that can cause data loss type the following**

```dj
docker stop -t 0 docker_id
```

**docker rm comand removes only stopped containers**</br>

```dj
docker rm container_id
```

**to remove running container** </br>
```dj
docker rm -f container_id
```

**to get all the id of container in the docker list**

```dj
docker ps -aq
```

**to delete all the container in the list in linux system** </br>
```dj
docker ps -aq | xargs docker rm 


**to see all the docker images** </br>

```dj
docker images
```

**remove or force to remove images, if the docker is running stop it 
first then remove** </br>

```dj
docker rmi image_name
docker rmi -r image_name
```