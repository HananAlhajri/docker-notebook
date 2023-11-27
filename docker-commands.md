# docker commands

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

5. delete an image
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
  ** -it stands for 'interactive terminal'
  ** type 'exit' to exit from the terminal 
9. stop a container
```
docker stop container-id
```

# flags
<li> -d : detach mode</li>
<li> -p : ports </li>
<li> -it : interactive terminal </li>

# notes
  * some container do not have bash installed. Thus, if /bin/bash does not work, try /bin/sh
  * in order to delete an image you MUST stop containers that image is running in. Then, delete the container, finally, you can delete the image after that.


# great resources 
<li>https://www.youtube.com/watch?v=3c-iBn73dDE&list=PLy7NrYWoggjxtN4YbSMYFFdpaxb-fR4zC&index=1</li>
<li>https://www.ajfriesen.com/how-to-find-all-the-docker-run-flags/</li>
<li>https://www.baeldung.com/java-dockerize-app</li>
