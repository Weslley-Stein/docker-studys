# Volumes

Volumes is useful becauses everytime you restart all the data inside him just gone, so if you want do keep that data you need to create and manage volumes

### Options

* --mount: create a volume
	* --mount type=[type]: specify the type of volume(the default is "volume")
	* --mount src=[dir]: will specify which directory we want to put inside the container.
	* --mount dst=[dir]: will specify the path where we will put the src dir inside the container
	* --mount ro: read-only option to prevent do edit the filesystem inside the container 

### Full Command Example:

```docker
docker container run -ti --mount type=bind,src=/dir1,dst=/dir2 ubuntu
```

### Creating a new volume

The volume will be stored on "/var/lib/docker/volumes"
```docker
docker volume create [name]
```

### Delete a volume

```docker
docker volume rm [name]
```

Next Lesson:[[dockerfile]]
