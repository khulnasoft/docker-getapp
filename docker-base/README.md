# Docker Base

[![Discord](https://img.shields.io/discord/564160730845151244?label=discord&style=flat-square)](https://khulnasoft.com/discord)
[![Docker Pulls](https://img.shields.io/docker/pulls/khulnasoft/base?color=f02e65&style=flat-square)](https://hub.docker.com/r/khulnasoft/base)
[![Build Status](https://img.shields.io/travis/com/getapp/docker-base?style=flat-square)](https://travis-ci.com/getapp/docker-base)
[![Twitter Account](https://img.shields.io/twitter/follow/getapp?color=00acee&label=twitter&style=flat-square)](https://twitter.com/getapp)
[![Follow GetApp on StackShare](https://img.shields.io/badge/follow%20on-stackshare-blue?style=flat-square)](https://stackshare.io/getapp)

[GetApp](https://khulnasoft.com) base docker image with applications and extensions built and installed.

## Getting Started

These instructions will cover usage information to help your run GetApp's base docker container.

### Prerequisites

In order to run this container you'll need docker installed.

* [Windows](https://docs.docker.com/windows/started)
* [OS X](https://docs.docker.com/mac/started/)
* [Linux](https://docs.docker.com/linux/started/)

### Usage

```shell
docker run khulnasoft/base
```

### Testing

We use [Container Structure Test](https://github.com/GoogleContainerTools/container-structure-test) to run test for the docker image. In order to run test first install Container strucutre test using the following command.

```bash
curl -LO https://storage.googleapis.com/container-structure-test/latest/container-structure-test-linux-amd64 && chmod +x container-structure-test-linux-amd64 && sudo mv container-structure-test-linux-amd64 /usr/local/bin/container-structure-test
```

### Run Test

First build and tag the docker image and then run the test using the configuration file.

```bash
docker build -t getapp-base-test .
container-structure-test test --config tests.yaml --image getapp-base-test
```

### Build

```bash
docker build --tag khulnasoft/base:1.0.0 .

docker push khulnasoft/base:1.0.0
```

Multi-arch build (using [buildx](https://github.com/docker/buildx)):

```
docker buildx build --platform linux/amd64,linux/arm64/v8,linux/ppc64le --tag khulnasoft/base:1.0.0 --push .
```

## Find Us

* [GitHub](https://github.com/khulnasoft)
* [Discord](https://khulnasoft.com/discord)
* [Twitter](https://twitter.com/khulnasoft)

## Copyright and license

The MIT License (MIT) [http://www.opensource.org/licenses/mit-license.php](http://www.opensource.org/licenses/mit-license.php)