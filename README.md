## Supervisor Dockerfile

This repository contains **Dockerfile** of [Supervisor](http://supervisord.org/) for [Docker](https://www.docker.com/)'s [automated build](https://registry.hub.docker.com/u/kdelfour/supervisor-docker/) published to the public [Docker Hub Registry](https://registry.hub.docker.com/).

### Base Docker Image

* [aarch64/ubuntu](http://dockerfile.github.io/r/aarch64/ubuntu)

### Installation

1. Install [Docker](https://www.docker.com/).

2. Download [build](https://registry.hub.docker.com/u/wgbartley/aarch64-supervisor-docker/) from public [Docker Hub Registry](https://registry.hub.docker.com/): `docker pull wgbartley/aarch64-supervisor-docker`

   (alternatively, you can build an image from Dockerfile: `docker build -t="wgbartley/aarch64-supervisor-docker" https://github.com/wgbartley/aarch64-supervisor-docker`)

### Usage

    docker run -it --rm wgbartley/aarch64-supervisor-docker

#### Run with custom config directory

    docker run -d -v <config-dir>:/etc/supervisor/conf.d wgbartley/aarch64-supervisor-docker

### Credit

This image was built from the original kdelfour/supervisor-docker image with minor tweaks
to work with aarch64/ubuntu (for original intended use on a Pine 64 single board computer).
