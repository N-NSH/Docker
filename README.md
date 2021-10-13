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

# Error checking TLS connection: Host is not running
# Solution: 

`$ docker-machine start default`

`$ docker-machine env default`

`$ eval $(docker-machine env default)`
