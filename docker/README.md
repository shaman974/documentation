# DOCKER

## Documentation

## Ligne

### Option générique

-d : detaché

-a : tout

### Compose

lancement d'un docker compose

```
docker-compose up
```
lancement d'un docker avec build

```
docker-compose up --build
```

arret du docker compose

```
docker-compose down
```

### Docker

#### Build de l'image

```
docker build .
```

Forcer le nom de l'image :

-t

```
docker build . -t <NOM_CONTENER>
```

#### Log


```
docker logs <CONTAINER>
```
-f : suivre les logs

```
docker logs <CONTAINER> -f
```

https://docs.docker.com/engine/reference/commandline/logs/
