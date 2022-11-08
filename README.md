# traefik-portainer-dockerswarm
Example stack

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