# Docker Secrets

### Commands
- docker secret ls: will list all the secrets
- docker secret inspect SECRETNAME: will give us information about the secret
- docker secret rm SECRETNAME: will remove a secret 
- docker secret create: will create a secret

### Creating a secret
```docker
docker secret create --name NAME FILE
echo "string" | docker secret create --name -
```

### OBS
1. Secrets its storaged inside the filesystem of the container on the path /run/secrets/SECRETNAME
