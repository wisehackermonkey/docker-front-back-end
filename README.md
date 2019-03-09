# Docker ci experiment
[![Build Status](https://travis-ci.com/wisehackermonkey/docker-front-back-end.svg?branch=master)](https://travis-ci.com/wisehackermonkey/docker-front-back-end)

###  use travis ci to build docker containers and host them on dockerhub

-----

Build
```
>docker-compose -f ./docker-compose-build.yml pull
>docker-compose -f ./docker-compose-build.yml build
>docker-compose ps
```
## Run
###### run in forground
```bash
docker-compose up
```
###### run in background (recommended)
```bash
>docker-compose up -d
```
## Deploy
###### install and run. NOTE: running in linux docker and git are required to run in production
```bash
>cd ~
>git clone https://github.com/wisehackermonkey/docker-front-back-end.git
>cd ./docker-front-back-end
>bash ./deploy_service.sh
```
## Develope
###### build the project
```
>docker login
>docker-compose -f ./docker-compose-build.yml pull
>docker-compose -f ./docker-compose-build.yml build
>docker push wisehackermonkey/frontend:latest
>docker push wisehackermonkey/backend:latest
```
###### Run
```bash
>docker-compose up [-d]
```
