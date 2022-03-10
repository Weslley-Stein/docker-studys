### Installing Curl
```bash
root@fedora: yum install curl -y
```
### Installing Docker
```bash
root@fedora: curl -fsSl https://get.docker.com/
root@fedora: yum install docker-ce docker-ce-cli containerd.io
```

### Starting Docker and allowing it to start when the machine boot
```bash
root@fedora: systemctl start docker.service containerd.io
root@fedora: systemctl enable docker.service containerd.io
```

### Allowing to use docker without use sudo everytime
```bash
root@fedora: groupadd docker
root@fedora: usermod -a -G docker [username]
```

Next Lesson:[[basic-commands]]
