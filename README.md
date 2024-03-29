## Some useful docker commands

### list all containers
```shell
docker ps -a
```

### list images

```shell
docker images
```

### download image from hub

```shell
docker pull ubuntu:latest
```

### start container

```shell
docker start CONTAINER_ID
```

### stop container

```shell
docker stop CONTAINER_ID
```

### create a container from image and access it's terminal

```shell
docker run -it --entrypoint "/bin/bash" ubuntu
```

### access terminal from a running container

```shell
docker exec -it CONTAINER_ID bash
```

### remove container

```shell
docker rm CONTAINER_ID
```

### example setting environment variables

```shell
docker run --name postgres -e POSTGRES_PASSWORD=123456 -d -p 5432:5432 postgres
```

### copy file to container

```shell
docker cp file.txt CONTAINER_ID:/tmp/
```

### create image from a container

```shell
docker commit CONTAINER_ID
```

### tag image created

```shell
docker tag CONTAINER_ID tag_name
```

### create image with tag

```shell
docker commit CONTAINER_ID tag_name
```

### export image from docker

```shell
docker save image_name -o file.tar
```

### import image to docker

```shell
docker load -i file.tar
```