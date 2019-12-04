# Basic Docker commands

```sh
docker run nginx

# lists all running containers
docker ps

# lists all containers
docker ps -a

docker stop [cotiner id/name]

docker rm [cotiner id/name]

docker images

docker rmi [image id/name]

docker pull ubuntu

docker run ubuntu

docker run ubuntu sleep 30

docker exec [container id/name] cat /etc/hosts

```

### Run the container in datach mode
```sh
example:

docker run ubuntu

docker run ubuntu cat /etc/*release*

docker run ubuntu:16.04 cat /etc/*release*

docker ps

docker run ubuntu sleep 30

docker run -d ubuntu sleep 30

docker ps
```
### get inside the container
```sh
docker run -it centos bash
```

### EXEC
```sh
docker run -d ubuntu sleep 100

docker ps

docker exec [get id from the previous o/p] cat /etc/*release*
```

### TAG
```sh
# if you don't mention any tag, by default 'latest' will be pulled

docker run redis

# if you want to specify something

docker run redis:4.0
```
### attach & detach
```sh
use '-d' to run in the detahced mode i.e. in the background

docker run -d ubuntu sleep 1000

if you want to atatch it 

docker attach [cont-id]
```

### Port Mapping
```sh
docker run -p 800:5000 my-web-app

800 in my host
5000 on my container

So, you can access by using

http://host-ip:800/
```
### Data Persistence - Volume Mapping
```sh

```
