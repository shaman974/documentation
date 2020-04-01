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
docker build . -t perso-gateway
```