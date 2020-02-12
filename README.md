# HEIMDALL

<img src="https://assets.gitlab-static.net/uploads/-/system/project/avatar/13827678/heimdalllogo.png" width="300" height="200"/>

## INDEX

- [HEIMDALL](#heimdall)
  - [INDEX](#index)
  - [BADGES](#badges)
  - [INTRODUCTION](#introduction)
  - [PREREQUISITES](#prerequisites)
  - [INSTALL](#install)
  - [LICENSE](#license)

## BADGES

[![pipeline status](https://gitlab.com/oda-alexandre/heimdall/badges/master/pipeline.svg)](https://gitlab.com/oda-alexandre/heimdall/commits/master)

## INTRODUCTION

Docker image of :

- [heimdall](http://heimdall-download.com)

Continuous integration on :

- [gitlab](https://gitlab.com/oda-alexandre/heimdall/pipelines)

Automatically updated on :

- [docker hub public](https://hub.docker.com/r/alexandreoda/heimdall/)

## PREREQUISITES

- Use [docker](https://www.docker.com)

## INSTALL

```docker run -d --name heimdall -v ${HOME}:/home/heimdall -v /tmp/.X11-unix/:/tmp/.X11-unix/ -v /dev/bus/usb:/dev/bus/usb -e DISPLAY --privileged alexandreoda/heimdall```

## LICENSE

[![GPLv3+](http://gplv3.fsf.org/gplv3-127x51.png)](https://gitlab.com/oda-alexandre/heimdall/blob/master/LICENSE)
