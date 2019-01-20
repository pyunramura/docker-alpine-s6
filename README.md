# pyunramura/alpine-s6
[![](https://images.microbadger.com/badges/image/pyunramura/alpine-s6:3.8.svg)](https://microbadger.com/images/pyunramura/alpine-s6:3.8 "MicroBadger.com info on my Docker image")
[![](https://images.microbadger.com/badges/version/pyunramura/alpine-s6:3.8.svg)](https://hub.docker.com/r/pyunramura/alpine-s6 "Link to Docker Hub project")
[![](https://images.microbadger.com/badges/commit/pyunramura/alpine-s6:3.8.svg)](https://hub.docker.com/u/pyunramura "Link to my Docker Hub profile")
[![](https://img.shields.io/github/license/pyunramura/docker-alpine-s6.svg?logo=github&logoColor=white)](https://github.com/pyunramura/docker-alpine-s6/blob/master/LICENSE "Link to the license")
[![](https://img.shields.io/github/languages/top/pyunramura/docker-alpine-s6.svg?colorB=green&logo=docker&logoColor=white)](https://github.com/pyunramura/docker-alpine-s6 "Link to my Github project")

## How to use this image

This container is configured to work as a base image for other Docker containers to build on top of. It is based on [Alpine linux](https://alpinelinux.org/) with [s6-overlay](https://github.com/just-containers/s6-overlay).

![https://alpinelinux.org/](https://upload.wikimedia.org/wikipedia/commons/e/e6/Alpine_Linux.svg)

Alpine Linux is optimized to be extremely light on resources while maintaining the tools you would expect in a linux distribution with none of the fluff. In other words, it's built for Docker. Justcontiners s6-overlay is similarly optimized to maintain low resource usage while featuring robust process management. 
Additionally this container is heavily modeled after the fantastic [linuxserver.io](https://hub.docker.com/u/linuxserver/) containers, but with  slightly more aggressive space-saving techniques.

Feedback is welcome and encouraged as I'm always looking to improve my containers.

## Usage Example

```
docker run -d --rm --name=alpine pyunramura/alpine-s6
```

## Parameters

`The parameters below are split into two halves, separated by a colon, the left hand side representing the host and the right the container side.`

For example with `-p external:internal` - what this shows is the port mapping from external to internal of the container.
So -p 80:8080 would expose port 8080 from inside the container to be accessible from the host's IP on port 80
http://192.168.x.x:80 would show you what's running INSIDE the container on port 8080.

 * `-p 8080` - an example port for connecting to services on port 8080 of the container
 * `--name` - human readable alias you want to run this container under

## Info

* For shell access while the container is running

   `docker exec -it alpine /bin/sh`.

* To monitor the logs of the container in realtime

   `docker logs -f alpine`.

* For the container version number

   `docker inspect -f '{{ index .Config.Labels "build_version" }}' alpine`.

* For the image version number

   `docker inspect -f '{{ index .Config.Labels "build_version" }}' pyunramura/alpine`.

## Versions

+ **3.8** - Initial Release.

