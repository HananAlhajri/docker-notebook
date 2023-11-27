# Docker commands

1. list currently running containers
```
docker ps
```
2. build an image
```
docker build image-name:version
```
3. delete a container
```
docker rm container-id
```

5. delte an image
```
docker rmi image-id-or-name
```
5. list all images
```
docker images
```
6. start an image
```
docker run image-id-or-name
```
7. see the logs of a running container
```
docker logs container-id
```
8. to enter the container terminal
```
docker exec -it container-id /bin/bash
```
** Note:
  * some container do not have bash installed. Thus, if /bin/bash does not work, try /bin/sh
  * -it stands for 'interactive terminal'
