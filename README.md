# HEIMDALL

![logo](https://assets.gitlab-static.net/uploads/-/system/project/avatar/13827678/heimdalllogo.png)

## INDEX

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

## INSTALL

### DOCKER RUN

```\
docker  run -d --name heimdall -v ${HOME}:/home/heimdall -v /tmp/.X11-unix/:/tmp/.X11-unix/ -v /dev/bus/usb:/dev/bus/usb -e DISPLAY alexandreoda/heimdall
```

### DOCKER COMPOSE

```yml
version: "3.7"

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
