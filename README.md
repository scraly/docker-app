# docker-app

Experimental utility designed to make compose files shareable and reusable.

Creates a docker image containing:
- docker compose file
- settings and metadata files
- other supporting files

## Installation

```
$ wget https://github.com/docker/app/releases/download/v0.6.0/docker-app-linux.tar.gz
$ tar xf docker-app-linux.tar.gz
$ sudo cp docker-app-linux /usr/local/bin/docker-app
```

## Shell completion

### Bash

```
$ vi .bashrc
$ source <(docker-app completion bash)
```

### Zsh

```
$ vi .zshrc
$ source <(docker-app completion zsh
```

## Usage

### Bootstrap a project

`$ docker-app init test`

### Launch the application locally

`$ docker-app render | docker-compose -f - up`

### create an image and push it

`$ docker-app push --namespace myhubuser --tag latest`

### Pull the app and output the compose file to stdout

`$ docker-app render scraly/test.dockerapp:latest`

### pull the docker image and deploy it

`$ docker-app deploy scraly/test:latest`

After deploy command, docker image is available on [docker hub](https://hub.docker.com/r/scraly/test.dockerapp).
