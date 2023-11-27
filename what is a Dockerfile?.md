# What is a Dockerfile?
It is a blueprint for building images. To build docker image for an application, we need to copy the content of the application into the dockefile (the artifact we built 'jar, war, etc...'). 

### the first line of every dockerfile is: 
#### > FROM
whatever image your building you wanna base it on another image, such as -> node for node.js apps, jdk for java apps, and so on. 
###### use the right image
You can find the images on [hub.docker.com](https://hub.docker.com/)https://hub.docker.com/ 
Search for the image AND the version you need, or simply choose tha latest.

#### > ENV
to set the enviroment variables. 
such as: 

```
MONGO_DB_USERNAME=username \
MONGO_DB_PASSWORD=password
```
** NOTE THAT : it is an option, BUT it is better to write them in a docker-compose file. So instead of rebuilding the image, you can change the docker-compose file and override it.

#### > RUN
here you can execute any linux command -> example : mkdir -p /home/app
** NOTE THAT : this directory will be created and live INSIDE of the container not on the host

#### > COPY
this one executes on the HOST 
COPY . /home/app
. is the source , and /home/app is the target

#### > CMD 
is ALWAYS a part of dockerfile. what it does it executes an entry point linux command.

<img width="1918" alt="image" src="https://github.com/HananAlhajri/docker-compose/assets/92547643/6b35ae7e-3b59-4958-8f92-8f7cf12e5632">
the left side of the image illustrate what actually happens in the container, what it can do. As on the right side, the commands we've just gone through.

# How to build an image using your Dockerfile

using 'docker build' command, you have to give your image 2 parameters 
1. -t NAME : TAG (( could be anything of your choice -> ex: my-app-name:version-1 ))
2. location of a Dockerfile (( if you are standing on the same folder as the Dockerfile, just provide a 'dot' which means 'current directory' ))

```
docker build -t my-app:1.0 .
```

# Notes
<li>Whenever you adjust your Dockerfile, you MUST RE-BUILD the Image!</li>

