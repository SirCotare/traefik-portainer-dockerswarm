# traefik-portainer-dockerswarm
Example stack

## DNS Setup
Before you start your new stack, make sure that you have added DNS entries for your domain to point to the right server.

## Server Setup
Copy the infra.yml to your server and check the commented lines for things you have to change.

```
apt install docker.io
```

```
docker swarm init
```

```
docker network create --driver=overlay --scope=swarm traefik
```

```
docker stack deploy -c infra.yml infra
```

And then you hope :)

Traefik: https://traefik.yourdomain.com/dashboard/ (trailing slash required for some reason...)

Portainer: https://portainer.yourdomain.com

## Useful commands

```
docker stack ls
docker service ls
docker service logs [hash]
docker [command] --help
docker --help
```

Fyi: you don't need the full hash in the commands. 2-3 letters are sufficient as long as those are unique anyway.