# How to install docker and docker compose

## Install Docker Engine - Community

```
$ sudo apt-get update
```
```
$ sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg-agent \
    software-properties-common
```
```
$ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
```
```
$ sudo apt-get update
```
```
$ sudo apt-get install docker-ce docker-ce-cli containerd.io
```

## To test your installation
```
$ sudo docker run hello-world
```

##  Install Docker Compose
```
sudo curl -L "https://github.com/docker/compose/releases/download/1.24.1/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
```
```
sudo chmod +x /usr/local/bin/docker-compose
```
## Test the installation
```
$ docker-compose --version
docker-compose version 1.24.1, build 1110ad01
```
# How to use docker

## How to control docker service

We can user `$ sudo service docker ${command}` or we can use `$ sudo systemctl docker ${command}` for linux distribution like readhat or centos

**Start docker**

    $ sudo service docker start

**Stop docker**

    $ sudo service docker stop

**Reload docker**

    $ sudo service docker reload

**Restart docker** 

    $ sudo service docker restart

**Get docker status**

    $ sudo service docker status

## Container status

**Working container status**
  
      $ sudo docker ps
      
**All container status**

    $ sudo docker ps -a

## Control containers
 **Attach local standard input, output, and error streams to a running container**

    $ sudo docker container attach [OPTIONS] CONTAINER

**Create a new image from a container's changes**

     $ sudo docker container commit [OPTIONS] CONTAINER [REPOSITORY[:TAG]]

 **Copy files/folders between a container and the local filesystem**
 

    $ sudo docker container cp [OPTIONS] CONTAINER:SRC_PATH DEST_PATH|-

    $ sudo docker cp [OPTIONS] SRC_PATH|- CONTAINER:DEST_PATH

  **Create a new container**         

    $ sudo docker container create [OPTIONS] IMAGE [COMMAND] [ARG...]

**Inspect changes to files or directories on a container's filesystem**      
 

     $ sudo docker container diff CONTAINER

  **Run a command in a running container**     
  

    $ sudo docker container exec [OPTIONS] CONTAINER COMMAND [ARG...]

**Export a container's filesystem as a tar archive**

    $ sudo docker container export [OPTIONS] CONTAINER

**Display detailed information on one or more containers**

    $ sudo docker container inspect [OPTIONS] CONTAINER [CONTAINER...]

**Kill one or more running containers**

    $ sudo docker container kill [OPTIONS] CONTAINER [CONTAINER...]

**Fetch the logs of a container**

    $ sudo docker container logs [OPTIONS] CONTAINER

**List containers**

    $ sudo docker container ls

**Pause all processes within one or more containers**

    $ sudo docker container pause CONTAINER [CONTAINER...]

**List port mappings or a specific mapping for the container**

    $ sudo docker container port CONTAINER [PRIVATE_PORT[/PROTO]]

**Remove all stopped containers**

    $ sudo docker container prune

**Rename a container**

    $ sudo docker container rename CONTAINER NEW_NAME

**Restart one or more containers**

    $ sudo docker container restart [OPTIONS] CONTAINER [CONTAINER...]

**Remove one or more containers**

    $ sudo docker container rm [OPTIONS] CONTAINER [CONTAINER...]

**Run a command in a new container**

    $ sudo docker container run [OPTIONS] IMAGE [COMMAND] [ARG...]

**Start one or more stopped containers**

    $ sudo docker container start [OPTIONS] CONTAINER [CONTAINER...]

**Display a live stream of container(s) resource usage statistics**

    $ sudo docker container stats

**Stop one or more running containers**

    $ sudo docker container stop [OPTIONS] CONTAINER [CONTAINER...]

**Display the running processes of a container**

    $ sudo docker container top

**Unpause all processes within one or more containers**

    $ sudo docker container unpause CONTAINER [CONTAINER...]

**Update configuration of one or more containers**

    $ sudo docker container update [OPTIONS] CONTAINER [CONTAINER...]

**Block until one or more containers stop, then print their exit codes**

    $ sudo docker container wait CONTAINER [CONTAINER...]
## Docker image
**Gets a list of downloaded image in your local registry**

    $ sudo docker images

**Download image from dockerhub registry**

    $ sudo docker pull IMAGE NAME

**Upload image into docker hub registry**

    $ sudo docker push IMAGE NAME

**Remove image from your local registry**

    $ sudo docker rmi IMAGE_NAME OR ID