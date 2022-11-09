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

Traefik: https://traefik.yourdomain.com/dashboard/

Portainer: https://portainer.yourdomain.com
