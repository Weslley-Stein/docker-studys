## Type of commands
On Docker the most used types of commands is Container Commands and Images Commands, i will explain that with details on this file

## Container Commands

### See all running containers:

```docker
docker container ls
```

### See every container(even if his isnt running):

```docker 
docker container ls -l
```

### Run a container based on the specified image and interact with it using the terminal:
 
```docker
docker container run -ti [image]
```

### Rename a container:

```docker
docker container rename [containerID/containerNAME]
```

### Get informations about the container:

```docker
docker container inspect [containerID/containerNAME]
```

### Get Hardware informations about the container:

```docker
docker container stats [containerID/containerNAME]
```

### Interact with a running container terminal(But just if his main process is the Bash):

```docker
docker container attach [containerID/containerNAME]
```


