# Docker MariaDB

[![Discord](https://img.shields.io/discord/564160730845151244?label=discord&style=flat-square)](https://khulnasoft.com/discord)
[![Docker Pulls](https://img.shields.io/docker/pulls/khulnasoft/getapp-mariadb?color=f02e65&style=flat-square)](https://hub.docker.com/r/khulnasoft/getapp-mariadb)
[![Build Status](https://img.shields.io/travis/com/khulnasoft/docker-mariadb?style=flat-square)](https://travis-ci.com/khulnasoft/docker-mariadb)
[![Twitter Account](https://img.shields.io/twitter/follow/khulnasoft?color=00acee&label=twitter&style=flat-square)](https://twitter.com/khulnasoft)
[![Follow GetApp on StackShare](https://img.shields.io/badge/follow%20on-stackshare-blue?style=flat-square)](https://stackshare.io/getapp)

MariaDB container with [GetApp server](https://khulnasoft.com) DB schema and tables initialized and ready to use for fresh GetApp installation. This server is only extending the official MariaDB docker image with GetApp schemas and tables already installed, for a fresh installation of MariaDB use only [docker official image](https://hub.docker.com/_/mariadb).

## Getting Started

These instructions will cover usage information to help your run GetApp's MariaDB docker container.

### Prerequisites

In order to run this container you'll need docker installed.

* [Windows](https://docs.docker.com/windows/started)
* [OS X](https://docs.docker.com/mac/started/)
* [Linux](https://docs.docker.com/linux/started/)

### Usage

```shell
docker run khulnasoft/getapp-mariadb
```

### Environment Variables

This container supports all environment variables supplied by the official MariaDB Docker image.

### Build

```bash
docker build --tag khulnasoft/getapp-mariadb:1.3.0 .

docker push khulnasoft/getapp-mariadb:1.3.0
```

Multi-arch build (experimental using [buildx](https://github.com/docker/buildx)):

```
docker buildx build --platform linux/amd64,linux/arm64/v8,linux/ppc64le --tag khulnasoft/getapp-mariadb:1.3.0 --push .
```

## Find Us

* [GitHub](https://github.com/khulnasoft)
* [Discord](https://khulnasoft.com/discord)
* [Twitter](https://twitter.com/khulnasoft)

## Copyright and license

The MIT License (MIT) [http://www.opensource.org/licenses/mit-license.php](http://www.opensource.org/licenses/mit-license.php)