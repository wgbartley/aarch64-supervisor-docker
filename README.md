## Supervisor Dockerfile

This repository contains **Dockerfile** of [Supervisor](http://supervisord.org/) for [Docker](https://www.docker.com/)'s [automated build](https://registry.hub.docker.com/u/kdelfour/supervisor-docker/) published to the public [Docker Hub Registry](https://registry.hub.docker.com/).

### Base Docker Image

* [dockerfile/ubuntu](http://dockerfile.github.io/#/ubuntu)

### Installation

1. Install [Docker](https://www.docker.com/).

2. Download [automated build](https://registry.hub.docker.com/u/kdelfour/supervisor-docker/) from public [Docker Hub Registry](https://registry.hub.docker.com/): `docker pull kdelfour/supervisor-docker`

   (alternatively, you can build an image from Dockerfile: `docker build -t="kdelfour/supervisor-docker" https://github.com/kdelfour/supervisor-docker`)

### Usage

    docker run -it --rm kdelfour/supervisor-docker

#### Run with custom config directory

    docker run -d -v <config-dir>:/etc/supervisor/conf.d kdelfour/supervisor-docker