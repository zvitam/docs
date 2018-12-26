<!--

********************************************************************************

WARNING:

    DO NOT EDIT "alpine/README.md"

    IT IS AUTO-GENERATED

    (from the other files in "alpine/" combined with a set of templates)

********************************************************************************

-->

# Supported tags and respective `Dockerfile` links

-	[`3.6` (*versions/library-3.6/s390x/Dockerfile*)](https://github.com/gliderlabs/docker-alpine/blob/0b3a938c6c79161773e3fce02bcf224a3ba5adb5/versions/library-3.6/s390x/Dockerfile)
-	[`3.7` (*versions/library-3.7/s390x/Dockerfile*)](https://github.com/gliderlabs/docker-alpine/blob/32992d93a7c6e2f20febe09ada3edffc784cd2ce/versions/library-3.7/s390x/Dockerfile)
-	[`3.8`, `latest` (*versions/library-3.8/s390x/Dockerfile*)](https://github.com/gliderlabs/docker-alpine/blob/9fa40ec5fe4be402751c441e6e89eef390e29427/versions/library-3.8/s390x/Dockerfile)
-	[`edge` (*versions/library-edge/s390x/Dockerfile*)](https://github.com/gliderlabs/docker-alpine/blob/2e66ab5ff57fc12512a099706c90b833f186b7b9/versions/library-edge/s390x/Dockerfile)

[![Build Status](https://doi-janky.infosiftr.net/job/multiarch/job/s390x/job/alpine/badge/icon) (`s390x/alpine` build job)](https://doi-janky.infosiftr.net/job/multiarch/job/s390x/job/alpine/)

# Quick reference

-	**Where to get help**:  
	[the Docker Community Forums](https://forums.docker.com/), [the Docker Community Slack](https://blog.docker.com/2016/11/introducing-docker-community-directory-docker-community-slack/), or [Stack Overflow](https://stackoverflow.com/search?tab=newest&q=docker)

-	**Where to file issues**:  
	[https://github.com/gliderlabs/docker-alpine/issues](https://github.com/gliderlabs/docker-alpine/issues)

-	**Maintained by**:  
	[Glider Labs](https://github.com/gliderlabs/docker-alpine) (an Alpine community contributor)

-	**Supported architectures**: ([more info](https://github.com/docker-library/official-images#architectures-other-than-amd64))  
	[`amd64`](https://hub.docker.com/r/amd64/alpine/), [`arm32v6`](https://hub.docker.com/r/arm32v6/alpine/), [`arm64v8`](https://hub.docker.com/r/arm64v8/alpine/), [`i386`](https://hub.docker.com/r/i386/alpine/), [`ppc64le`](https://hub.docker.com/r/ppc64le/alpine/), [`s390x`](https://hub.docker.com/r/s390x/alpine/)

-	**Published image artifact details**:  
	[repo-info repo's `repos/alpine/` directory](https://github.com/docker-library/repo-info/blob/master/repos/alpine) ([history](https://github.com/docker-library/repo-info/commits/master/repos/alpine))  
	(image metadata, transfer size, etc)

-	**Image updates**:  
	[official-images PRs with label `library/alpine`](https://github.com/docker-library/official-images/pulls?q=label%3Alibrary%2Falpine)  
	[official-images repo's `library/alpine` file](https://github.com/docker-library/official-images/blob/master/library/alpine) ([history](https://github.com/docker-library/official-images/commits/master/library/alpine))

-	**Source of this description**:  
	[docs repo's `alpine/` directory](https://github.com/docker-library/docs/tree/master/alpine) ([history](https://github.com/docker-library/docs/commits/master/alpine))

-	**Supported Docker versions**:  
	[the latest release](https://github.com/docker/docker-ce/releases/latest) (down to 1.6 on a best-effort basis)

# What is Alpine Linux?

[Alpine Linux](https://alpinelinux.org/) is a Linux distribution built around [musl libc](https://www.musl-libc.org/) and [BusyBox](https://www.busybox.net/). The image is only 5 MB in size and has access to a [package repository](https://pkgs.alpinelinux.org/) that is much more complete than other BusyBox based images. This makes Alpine Linux a great image base for utilities and even production applications. [Read more about Alpine Linux here](https://alpinelinux.org/about/) and you can see how their mantra fits in right at home with Docker images.

![logo](https://raw.githubusercontent.com/docker-library/docs/781049d54b1bd9b26d7e8ad384a92f7e0dcb0894/alpine/logo.png)

# How to use this image

## Usage

Use like you would any other base image:

```dockerfile
FROM s390x/alpine:3.7
RUN apk add --no-cache mysql-client
ENTRYPOINT ["mysql"]
```

This example has a virtual image size of only 36.8MB. Compare that to our good friend Ubuntu:

```dockerfile
FROM ubuntu:18.04
RUN apt-get update \
    && apt-get install -y --no-install-recommends mysql-client \
    && rm -rf /var/lib/apt/lists/*
ENTRYPOINT ["mysql"]
```

This yields us a virtual image size of about 145MB image.

## Documentation

This image is well documented. [Check out the documentation at Viewdocs](http://gliderlabs.viewdocs.io/docker-alpine).

# License

View [license information](https://pkgs.alpinelinux.org) for the software contained in this image.

As with all Docker images, these likely also contain other software which may be under other licenses (such as Bash, etc from the base distribution, along with any direct or indirect dependencies of the primary software being contained).

Some additional license information which was able to be auto-detected might be found in [the `repo-info` repository's `alpine/` directory](https://github.com/docker-library/repo-info/tree/master/repos/alpine).

As for any pre-built image usage, it is the image user's responsibility to ensure that any use of this image complies with any relevant licenses for all software contained within.
