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
