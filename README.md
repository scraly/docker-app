# docker-app

Experimental utility designed to make compose files shareable and reusable.

Creates a docker image containing:
- docker compose file
- settings and metadata files
- other supporting files

## Usage

### Bootstrap a project

`$ docker-app init test`

### create an image and push it

`$ docker-app push test`

### pull the docker imzge and deploy it

`$ docker-app deploy scraly/test:master`

### Pull the app and output the compose file to stdout

`$ docker-app render scraly/test.dockerapp:master`
