# tau-base-docker
Avidan Lab Docker Cheatsheet

This is a basic docker file and docker image, some explanations of how to 
build it and how to work with it.



# Setup
Create a directory shared with the docker

# Build docker Image
```bash
docker image build -t ajevnisek/tau-base-docker .
```

# Run docker Container
```bash
docker run --rm --name docker-demo -dit ajevnisek/tau-base-docker bash
```

## Watch dockers list:
```bash
docker container ls
```

## Kill docker Container:
```bash
docker kill <docker-id>
```

## Debug
### watch logs
```bash
docker logs docker-demo -f
```

### bash to the container
```bash
docker exec -it docker-demo bash
```


# Misc

Push docker to `docker.io`:
```bash
docker push ajevnisek/tau-base-docker:latest
```

Clear all docker cache:
```bash
docker system prune -a
```

# Run this image with run:ai:
```bash
runai submit -g 1 --name base-docker-demo -i ajevnisek/tau-base-docker --pvc=storage:/storage
```