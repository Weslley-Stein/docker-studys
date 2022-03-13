# Docker Swarm

Basically Docker Swarm its a Orchestration Container Tool, which allows you to create and manage Cluster

### commands
- docker swarm init: Initialize a Swarm
- docker swarm join: will init the swarm and make your machine a node of a cluster managed by a Leader
- docker swarm join-token manager: will give you a token for managers node come in as a manager in you cluster
- docker swarm join-token worker: will give you a token for workers node come in as a worker in your cluster
- docker swarm leave: will "shutdown" a node from the cluster(if he is a manager, its necessary to use the option "-f") 
- docker node ls: will show any node on your cluster
- docker node promote NODE: will promotes a node as a "Reachable" node, which means if the leader fall the "Reachable node" will be promoted as Leader 
- docker node demote NODE: will demote a node as a worker
- docker node rm NODE: will remove a node
- docker node inspect: will inspect a node 

### Options:

- -f: will force an action
- --advertise-addr IP: will specify an IP for the swarm init
- --rotate: will change the token of manager or worker for security porposes 
