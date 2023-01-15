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

**then run the container**

```dj
docker run name_of_the_container
```


**using another build with serverdocker file this time slight chnage in command**

```dj
docker build --file server.Dockerfile --tag name_of_container .
```

**don't use docker run container_name when the container is server or never stops
otherwise it will hang**

