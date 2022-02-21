# What's a Container?

Basically a container is an isolation, a physical isolation(CPU, Memory, Disk) and also logical(Processes, users and even network) which is possible
thanks to three Kernel Modules of Linux: Namespaces(who isolate the processes), Cgroups(who isolate the computational resources) and Netfilter(who isolate thenetwork)

# Which is the difference between a virtual machine and a container?

The most relavant difference is the size, virtual machines are pretty heavy they can weigh Gigabytes which make the backup and deploy slow on another hand
container is pretty lightweigh they have just some Megabytes, and the reason for that its because they doesnt have they own operational system neither kernel
they will use the host operational system and kernel

# What's Docker?

Docker basically is the tool who will allow you to Create and Manage you containers
