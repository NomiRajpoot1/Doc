## Volumes

[Volumes in Docker](https://docs.docker.com/engine/storage/volumes/)


## 

Commands to create volumes

```bash
  docker volume create nomi
```
Check the list of volume
```bash
  docker volume ls
```

Check new created volume data

```bash
  docker volume inspect nomi
```

Mount volume to the container | default path of volumes
```bash
  docker run -dt -p8888:80 -v /var/lib/docker/volumes/nomi:/usr/share/nginx/html nginx
```


## Methods to mount volume

- -v 
```bash
docker run -d \
  --name devtest \
  -v myvol2:/app \
  nginx:latest
```
- --mount
```bash 
 docker run -d \
  --name devtest \
  --mount source=myvol2,target=/app \
  nginx:latest
```
