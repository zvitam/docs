<!--

********************************************************************************

WARNING:

    DO NOT EDIT "elixir/README.md"

    IT IS AUTO-GENERATED

    (from the other files in "elixir/" combined with a set of templates)

********************************************************************************

-->

# Supported tags and respective `Dockerfile` links

-	[`1.7.4`, `1.7`, `latest` (*1.7/Dockerfile*)](https://github.com/c0b/docker-elixir/blob/7c1f05ca3fd47bdc86cab3f0310068646a31dcac/1.7/Dockerfile)
-	[`1.7.4-slim`, `1.7-slim`, `slim` (*1.7/slim/Dockerfile*)](https://github.com/c0b/docker-elixir/blob/7c1f05ca3fd47bdc86cab3f0310068646a31dcac/1.7/slim/Dockerfile)
-	[`1.6.6`, `1.6` (*1.6/Dockerfile*)](https://github.com/c0b/docker-elixir/blob/0936291249c7e11d4618a17a2b452045c9e6233a/1.6/Dockerfile)
-	[`1.6.6-slim`, `1.6-slim` (*1.6/slim/Dockerfile*)](https://github.com/c0b/docker-elixir/blob/0936291249c7e11d4618a17a2b452045c9e6233a/1.6/slim/Dockerfile)
-	[`1.6.6-otp-21`, `1.6-otp-21` (*1.6/otp-21/Dockerfile*)](https://github.com/c0b/docker-elixir/blob/b57a72d04ddd1f1b4e2e3f5b70e44e37def4db31/1.6/otp-21/Dockerfile)
-	[`1.5.3`, `1.5` (*1.5/Dockerfile*)](https://github.com/c0b/docker-elixir/blob/f2528c0158d465f96f311faa19aff3cffb4e7f25/1.5/Dockerfile)
-	[`1.5.3-slim`, `1.5-slim` (*1.5/slim/Dockerfile*)](https://github.com/c0b/docker-elixir/blob/f2528c0158d465f96f311faa19aff3cffb4e7f25/1.5/slim/Dockerfile)
-	[`1.4.5`, `1.4` (*1.4/Dockerfile*)](https://github.com/c0b/docker-elixir/blob/8f1888ae05506b9ad12e1b97f084a15e7588f442/1.4/Dockerfile)
-	[`1.4.5-slim`, `1.4-slim` (*1.4/slim/Dockerfile*)](https://github.com/c0b/docker-elixir/blob/8f1888ae05506b9ad12e1b97f084a15e7588f442/1.4/slim/Dockerfile)

[![Build Status](https://doi-janky.infosiftr.net/job/multiarch/job/arm32v7/job/elixir/badge/icon) (`arm32v7/elixir` build job)](https://doi-janky.infosiftr.net/job/multiarch/job/arm32v7/job/elixir/)

# Quick reference

-	**Where to get help**:  
	[the Docker Community Forums](https://forums.docker.com/), [the Docker Community Slack](https://blog.docker.com/2016/11/introducing-docker-community-directory-docker-community-slack/), or [Stack Overflow](https://stackoverflow.com/search?tab=newest&q=docker)

-	**Where to file issues**:  
	[https://github.com/c0b/docker-elixir/issues](https://github.com/c0b/docker-elixir/issues)

-	**Maintained by**:  
	[the Docker Community](https://github.com/c0b/docker-elixir), [with Elixir's support](https://github.com/docker-library/official-images/pull/1398#issuecomment-180484549)

-	**Supported architectures**: ([more info](https://github.com/docker-library/official-images#architectures-other-than-amd64))  
	[`amd64`](https://hub.docker.com/r/amd64/elixir/), [`arm32v7`](https://hub.docker.com/r/arm32v7/elixir/), [`arm64v8`](https://hub.docker.com/r/arm64v8/elixir/), [`i386`](https://hub.docker.com/r/i386/elixir/), [`ppc64le`](https://hub.docker.com/r/ppc64le/elixir/), [`s390x`](https://hub.docker.com/r/s390x/elixir/)

-	**Published image artifact details**:  
	[repo-info repo's `repos/elixir/` directory](https://github.com/docker-library/repo-info/blob/master/repos/elixir) ([history](https://github.com/docker-library/repo-info/commits/master/repos/elixir))  
	(image metadata, transfer size, etc)

-	**Image updates**:  
	[official-images PRs with label `library/elixir`](https://github.com/docker-library/official-images/pulls?q=label%3Alibrary%2Felixir)  
	[official-images repo's `library/elixir` file](https://github.com/docker-library/official-images/blob/master/library/elixir) ([history](https://github.com/docker-library/official-images/commits/master/library/elixir))

-	**Source of this description**:  
	[docs repo's `elixir/` directory](https://github.com/docker-library/docs/tree/master/elixir) ([history](https://github.com/docker-library/docs/commits/master/elixir))

-	**Supported Docker versions**:  
	[the latest release](https://github.com/docker/docker-ce/releases/latest) (down to 1.6 on a best-effort basis)

# What is Elixir?

Elixir is a dynamic, functional language designed for building scalable and maintainable applications.

Elixir leverages the Erlang VM, known for running low-latency, distributed and fault-tolerant systems, while also being successfully used in web development and the embedded software domain.

> [en.wikipedia.org/wiki/Elixir_(programming_language)](https://en.wikipedia.org/wiki/Elixir_%28programming_language%29)

![logo](https://raw.githubusercontent.com/docker-library/docs/f3ee5318992592f987a289cd72d63ac1807f569d/elixir/logo.png)

# How to use this image

## Run it as the REPL

```console
➸ docker run -it --rm arm32v7/elixir
Erlang/OTP 18 [erts-7.2.1] [source] [64-bit] [smp:8:8] [async-threads:10] [hipe] [kernel-poll:false]

Interactive Elixir (1.2.1) - press Ctrl+C to exit (type h() ENTER for help)
iex(1)> System.version
"1.2.1"
iex(2)>
➸ docker run -it --rm -h elixir.local arm32v7/elixir iex --sname snode
Erlang/OTP 18 [erts-7.2.1] [source] [64-bit] [smp:8:8] [async-threads:10] [hipe] [kernel-poll:false]

Interactive Elixir (1.2.1) - press Ctrl+C to exit (type h() ENTER for help)
iex(snode@elixir)1> System.version
"1.2.1"
iex(snode@elixir)2> :c.uptime
14 seconds
:ok
```

## Run a single Elixir exs script

```console
$ docker run -it --rm --name elixir-inst1 -v "$PWD":/usr/src/myapp -w /usr/src/myapp arm32v7/elixir elixir your-escript.exs
```

# Image Variants

The `arm32v7/elixir` images come in many flavors, each designed for a specific use case.

## `arm32v7/elixir:<version>`

This is the defacto image. If you are unsure about what your needs are, you probably want to use this one. It is designed to be used both as a throw away container (mount your source code and start the container to start your app), as well as the base to build other images off of.

## `arm32v7/elixir:<version>-slim`

This image does not contain the common packages contained in the default tag and only contains the minimal packages needed to run `arm32v7/elixir`. Unless you are working in an environment where *only* the `arm32v7/elixir` image will be deployed and you have space constraints, we highly recommend using the default image of this repository.

# License

Copyright 2012 Plataformatec

Licensed under the Apache License, Version 2.0 (the "License"); you may not use this file except in compliance with the License. You may obtain a copy of the License at

View [license information](http://www.apache.org/licenses/LICENSE-2.0) for the software contained in this image.

Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the License.

As with all Docker images, these likely also contain other software which may be under other licenses (such as Bash, etc from the base distribution, along with any direct or indirect dependencies of the primary software being contained).

Some additional license information which was able to be auto-detected might be found in [the `repo-info` repository's `elixir/` directory](https://github.com/docker-library/repo-info/tree/master/repos/elixir).

As for any pre-built image usage, it is the image user's responsibility to ensure that any use of this image complies with any relevant licenses for all software contained within.
