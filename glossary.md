# Glossary(All the commands and Options which i had learn)
All the commands of docker start with the prefix "docker", example of command with command, subcommand and option
```docker
docker container rm -f CONTAINERNAME
```
---
### Type of commands
- docker container(commands applied for containers)
- docker volume(commands applied for volumes)
- docker image(commands applied for images)
- docker swarm(command applied for Swarm/Clusters)i
- docker node(command applied for nodes)
- docker network(command applied for networks)
- docker secret(command applied for secrets)
---
### Subcommands
- docker container
	- rm CONTAINERNAME/ID: will remove a container
	- inspect CONTAINERNAME/ID: will inspect a container(all information about the container)
	- stats CONTAINERNAME/ID: will show you memory, disk, cpu and network usage
	- start CONTAINERNAME/ID: will start a container
	- stop CONTAINERNAME/ID: will stop a container
	- restart CONTAINERNAME/ID: will stop and then start a container
	- top CONTAINERNAME/ID: will show the main process of the containers:
	- logs CONTAINERNAME/ID: will show you the logs of the container
	- ls CONTAINERNAME/ID: will show you every container which is running
	- prune CONTAINERNAME/ID: will remove every stopped container
	- pause CONTAINERNAME/ID: will stop every process of a container
	- unpause CONTAINERNAME/ID: will start all the process of a pause container
	- exec CONTAINERNAME/ID: will execute a command as a main process of a container
	- update CONTAINERNAME/ID: will update one or more configurations of a container
	- attach CONTAINERNAME/ID: will attach the local stdin,stdout and stderr to a running container 
- docker image
	- ls : will show you every image
	- rm IMAGENAME/ID: will remove a specified image
	- prune: will remove useless images
	- build PATH/URL: will build a image based on a Dockerfile
	- tag IMAGENAME/ID name:tag : will put a name and a version on your image
- docker volume
	- create VOLUMENAME: will create a volume on /var/lib/docker/volumes/
	- ls: will list all your volumes
- docker swarm
	- init: will initialize your cluster
	- join-token manager: will give you a token for manager nodes
	- join-token worker: will give you a token for workers nodes
	- leave: will leave from cluster(if the node which is leaving is a manager its necessary to user the option "-f" to force the leaving)
	- join TOKEN: will join in a cluster
- docker node
	- promote: will promote a worker node as a manager
	- demote: will demote a manager node as worker
	- rm: will remove a node if he is stopped
---
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
- f: Will force an action
- a: Will show you "hidden" elements such as stoped containers or useless images
- --name: will give a name for the container, image or service
- --hostname: will specify the hostname of the container
- --pretty: will "prettify" the inspect output
