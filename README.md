# HEIMDALL

![logo](https://assets.gitlab-static.net/uploads/-/system/project/avatar/13827678/heimdalllogo.png)

- [HEIMDALL](#heimdall)
  - [INDEX](#index)
  - [BADGES](#badges)
  - [INTRODUCTION](#introduction)
  - [PREREQUISITES](#prerequisites)
  - [INSTALL](#install)
    - [DOCKER RUN](#docker-run)
    - [DOCKER COMPOSE](#docker-compose)
  - [LICENSE](#license)

## BADGES

[![pipeline status](https://gitlab.com/oda-alexandre/heimdall/badges/master/pipeline.svg)](https://gitlab.com/oda-alexandre/heimdall/commits/master)

## INTRODUCTION

Docker image of :

- [heimdall](http://heimdall-download.com)

Continuous integration on :

- [gitlab pipelines](https://gitlab.com/oda-alexandre/heimdall/pipelines)

Automatically updated on :

- [docker hub public](https://hub.docker.com/r/alexandreoda/heimdall/)

## PREREQUISITES

- Use [docker](https://www.docker.com)

## BUILD

### DOCKER RUN

```\
docker run -d \
--name heimdall \
-e DISPLAY \
-v ${HOME}:/home/heimdall \
-v /tmp/.X11-unix/:/tmp/.X11-unix/ \
-v /dev/bus/usb:/dev/bus/usb \
alexandreoda/heimdall
```

### DOCKER COMPOSE

```yml
version: "2.0"

services:
  heimdall:
    container_name: heimdall
    image: alexandreoda/heimdall
    restart: no
    network_mode: none
    privileged: false
    environment:
      - DISPLAY
    volumes:
      - "${HOME}:/home/heimdall"
      - "/tmp/.X11-unix/:/tmp/.X11-unix/"
      - "/dev/bus/usb:/dev/bus/usb"
```

## LICENSE

[![GPLv3+](http://gplv3.fsf.org/gplv3-127x51.png)](https://gitlab.com/oda-alexandre/heimdall/blob/master/LICENSE)
