# Container Commands

### See all running containers:

```docker
docker container ls
```

### See every container(even if his isnt running):

```docker 
docker container ls -a
```

### Rename a container:

```docker
docker container rename [containerID/containerNAME]
```

### Get informations about the container:

```docker
docker container inspect [containerID/containerNAME]
```

### See the heaviest process on the container
```docker
docker container top [containerID/containerNAME]
```

### Get Hardware informations about the container:

```docker
docker container stats [containerID/containerNAME]
```

### Show the logs of the container

```docker
docker container logs [containerID/containerNAME]
```

### Run a container based on the specified image and interact with it using the terminal:
 
```docker
docker container run -ti [image]
```

### Interact with a running container terminal(But just if his main process is the Bash):

```docker
docker container attach [containerID/containerNAME]
```

### Execute a command inside of a docker container

```docker
docker container exec [containerID/containerNAME] [command]
```

### Remove a container(you can use the option "-f" to force if the container is currently running)

```docker
docker container rm [containerID/containerNAME]
```

### Set a limit of memory and CPUs from you container

```docker
docker container run -m [quantity of memory in megabytes]M --cpus [number of cpus] [image]
```

### Change the limit of memory and CPUs from you container

```docker
docker container update -m [quantity of memory in megabytes]M --cpus [number of cpus] [containerID/containerNAME]
```

### Start, Restart or Stop you container

```docker
docker container start [containerID/containerNAME]
docker container restart [containerID/containerNAME]
docker container stop [containerID/containerNAME]
```

### Pause and Unpause you container

```docker
docker container pause [conainerID/containerNAME]
docker container unpause [containerID/containerNAME]
```


# Volume Commands


### Create a volume

```docker
docker volume create [name]
```

### Inspect a volume

```docker
docker volume inspect [name]
```

### Take an existing volume and attach it to a container

```docker
docker volume --mount type=volume,src=[volume],dst=[dir] [image]
```

Next Lesson:[[volumes]]
