# Docker Commands

## Cleaning out docker images
`docker system prune`

## Show all docker images
`docker images`

## Show all running docker containers
`docker ps` or `docker container ls`

## Build docker project with a Dockerfile into an image
`docker build -t {your-image-name} .`

## Kill a specific docker container
`docker kill {container-name}`

## Run docker image with detached option (runs in background)
`docker run -d --name {your-container-name} {docker-image-name}`

## Run docker image with detached option and attaching port 6379 and 8080
`docker run -d -p 6379:6379 -p 8080:8080 --name {your-container-name} {docker-image-name}`

## Execute a command in the docker container from outside the container
`docker exec {your-container-name} {your-command}`

## Copy a file from outside the docker container into the container
`docker cp {file-in-cuurr-dir} {container-name}:{to-directory}`

## Run docker container and enter file system
`docker run -it {image-name} /bin/bash`

## Custom tag docker container
`docker tag {local-image}:{tag-name} {new-repo}:{image-name}`

## Push docker image to Dockerhub
`docker push {new-repo}:{image-name}`
