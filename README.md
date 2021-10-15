# Docker Installation on Windows 8.1

1. First go to this link https://github.com/docker-archive/toolbox/releases and download the most recent .exe file of Docker Toolbox.
Note: Before installation make sure that Oracle VM Virtual Box is already removed otherwise you will face errors upon initialization of Docker Quick Start Terminal.
2. Use `docker info` to get the installation information
3. Whenever you pull an image the size of the disk.vmdk increases. You can check the disk in the following folder C:\Users\(username on pc)\.docker\machine\machines\default

#Docker Useful Commands
1. `docker version`
2. `docker-machine ls`
3. As we are running docker on VM not on windows directly to fix issues related error regarding docker version we can use the following commands:

> available command: `docker-machine help`

> `docker-machine env default` (it will list out all the commands for connecting to the default docker machine)

## Error checking TLS connection: Host is not running
## Solution: 

`$ docker-machine start default`

`$ docker-machine env default`

`$ eval $(docker-machine env default)`

## Docker Commands
`docker build -t tagname .`
short for --tag 

## Docker File Commands
`FROM <Repository>[<:tag>]`
  
`FROM <Repository>[<@digest>]`

- purpose of FROM instruction is to specify base image
- FROM instruction must be the first in a Dockerfile
- The argument must define a repository but a tag is optional
- Argument might refer to a digest, to specify the image

## How to run a container
`docker run  --name (name of the container) -it (name of the image)`

exmaple : `docker run --name test -it debian`

--name: Assign a name to the container

-it: The -it instructs Docker to allocate a pseudo-TTY connected to the container’s stdin; creating an interactive bash shell in the container.

`docker ps`

usage: All the containers running on your machine

`docker search image-name`

`docker pull image-name:tag-name`

## remove container
`docker stop container-name`

`docker rm container-name'

# CUDA
`nvdia-sm` can show memory usage, GPU utilization and temperature of GPU

## If you don't want to stop the container in linux OS, use ctrl + pq to exit the container


# VIM editor
1. :i : insert
2. :x : save file & exit 




## Running Docker using ConEmu(Cmder)
1. First you need to click on "create new console" then choose "set up tasks"
2. Under predefined tasks click on the +
3. Right click on the Docker Terminal shortcut and select the properties
4. Copy the the address from start in to the task parameter
5. Copy the target address to the command section 
6. Press save Settings
7. **Note:** Run the cmder as **administrator** then from the "create new console" select the defined task 


# Autor
Nooshin Noshiri

