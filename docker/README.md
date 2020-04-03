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

voir les images qui tournent

```
docker-compose images
```

voir les logs d'un docker compose (avec l'option pour voir le défilement)

```
docker-compose logs -f
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

#### Log d'un conteneur

```
docker logs <CONTAINER_ID>
```
-f : suivre les logs

```
docker logs <CONTAINER_ID> -f
```

https://docs.docker.com/engine/reference/commandline/logs/

#### Lancement d'un conteneur

#### Arret d'un conteneur

```
docker stop <CONTAINER_ID>
```
#### Consultation des conteneurs

Uniquement UP :

```
docker ps
```

Tous :

```
docker ps -a
```

#### Suppression d'un conteneur

```
docker rm <CONTAINER_ID>
```

#### Consulter les images

```
docker images
```

Toutes

```
docker images -a
```
#### Supprimer une image

```
docker rmi <IMAGES_ID>
```
