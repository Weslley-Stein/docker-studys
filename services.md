# Docker Services
Docker services its quite useful to scale to availability and also make a kind of Load Balancing, what he does is distribute containers as services among the Cluster

### Commands
- docker service create: will create a service
- docker service ls: will list running services
- docker service ps: will show you where each service is running
- docker service rm SERVICENAME: will remove a service
- docker service inspect SERVICENAME: will show you informations about the service
- docker service scale SERVICENAME=VALUE: will scale the number of services

### Creating a Service
```docker
docker service create --name NAME --replicas NUMBER -p PORTHOST:PORTGUEST IMAGE
```

### Options:
- --replicas: will specify the number of replicas(containers) for the service
- --mount: mount a volume for the service(which can be bind or volume)

# OBS:
1. When you bind a port on a service every replica will respond through the port of the service, doesnt matter which is his IP
