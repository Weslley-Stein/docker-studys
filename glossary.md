# Glossary(All the commands and Options which i had learn)

All the commands of docker start with the prefix "docker", and then we have


### Type of commands

- docker container(commands applied for containers)
- docker volume(commands applied for volumes)
- docker image(commands applied for images)


### Options

- -p: will bind two specified ports with each other
	```docker
		docker container run -p port1:port2 [...]
	```
- -P: if does exist a "EXPOSE" specification on the dockerfile who build the image, then we can bind a random port on the exposed port
	```docker
		docker container run -P [...]
	```
- -f: will force the execution of your command
	```docker
		docker container rm -f [...]
	```
- -t: will create a terminal for your container(a pseudo TTY)
- -i: will make your container interactive even if he isnt attached
- -d: will run your container on Daemon(on background)
- -v: its the old command to manipulate volumes, you need to give it a source and destination
	```docker
		docker container run -v /home/user/:/home/container/ [...] #This one is a Bind mount
		docker container run -v my_volume:/home/container/ [...] #And that one is a Volume Mount
	```
