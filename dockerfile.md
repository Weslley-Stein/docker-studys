# What's a Dockerfile?

Basiacally a dockerfile is a bunch of instrunctions to build a image

## Key Words and your pourpose

- FROM image (will specify on which OS or Image your container is based)
- WORKDIR "dir" (will set a default directory for the container)
- RUN "command" (will run a command on "docker run")
- COPY "localdir/file" "containerdir" (will copy files from your machine inside the container)
- ADD "localdir/file" "containerdir" (is the same as copy, but he is capable to take .tar files and put just the content inside the container 
- VOLUME "volume dir/name" (will create a volume)
- EXPOSE "port" (will expose a port to use it)
- CMD "command" will run a command when the container start
- ENV "NAME=VALUE" (will specify a environtment variable)
- ENTRYPOINT "[command]" (will specify the principal process of the container)

### OBS
1. we have two types of "CMD" the EXEC CMD which looks like this: CMD ["npm", "install"] who is "the most correct one" and we also have the shell CMD, which looks like; CMD command. If you already have an entrypoint so youneed to use the EXEC CMD 
