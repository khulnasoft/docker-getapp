# Docker ClamAV

[![Discord](https://img.shields.io/discord/564160730845151244?label=discord&style=flat-square)](https://khulnasoft.com/discord)
[![Docker Pulls](https://img.shields.io/docker/pulls/khulnasoft/getapp-clamav?color=f02e65&style=flat-square)](https://hub.docker.com/r/khulnasoft/getapp-clamav)
[![Twitter Account](https://img.shields.io/twitter/follow/khulnasoft?color=00acee&label=twitter&style=flat-square)](https://twitter.com/khulnasoft)
[![Follow GetApp on StackShare](https://img.shields.io/badge/follow%20on-stackshare-blue?style=flat-square)](https://stackshare.io/getapp)

A ClamAV docker image with auto database updates by the [KhulnaSoft team](https://github.com/khulnasoft). Use this image and a compatible client library to connect to the ClamAV using a TCP connection.

## Getting Started

These instructions will cover usage information to help your run ClamAV docker image 

### Prerequisities

In order to run this image you'll need docker installed.

* [Windows](https://docs.docker.com/windows/started)
* [OS X](https://docs.docker.com/mac/started/)
* [Linux](https://docs.docker.com/linux/started/)

### Usage

```shell
docker run khulnasoft/getapp-clamav
```

#### Environment Variables

This image has no environment variables. 

#### Volumes

You can mount any volume you need to allow the image to scan its files. 

### Build / Release

```
docker build --tag khulnasoft/getapp-clamav:0.0.0 .
docker push khulnasoft/getapp-clamav:0.0.0
```

Multi-arch build (experimental using [buildx](https://github.com/docker/buildx)):

```
docker buildx create --use
docker buildx build --platform linux/amd64,linux/arm/v6,linux/arm/v7,linux/arm64,linux/386,linux/ppc64le --tag khulnasoft/getapp-clamav:0.0.0 --push .
```

## Find Us

* [GitHub](https://github.com/khulnasoft)
* [Discord](https://khulnasoft.com/discord)
* [Twitter](https://twitter.com/khulnasoft)

## Copyright and license

The MIT License (MIT) [http://www.opensource.org/licenses/mit-license.php](http://www.opensource.org/licenses/mit-license.php)