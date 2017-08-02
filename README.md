# Base Docker Image

* [alpine](https://hub.docker.com/_/alpine/)

With [openjdk](https://hub.docker.com/_/openjdk/) as an addition to ensure the latest version of alpine and the openjdk 
are installed.


# Docker Tags

* 2.2.5 (latest)
[![](https://images.microbadger.com/badges/image/theidledeveloper/docker-gatling:2.2.5.svg)](https://microbadger.com/images/theidledeveloper/docker-gatling:2.2.5 "Get your own image badge on microbadger.com")

* latest
[![](https://images.microbadger.com/badges/image/theidledeveloper/docker-gatling.svg)](https://microbadger.com/images/theidledeveloper/docker-gatling "Get your own image badge on microbadger.com")


# Installation

* Install [Docker](https://www.docker.com/)

* Get automated build from public registry:

Latest version:

`docker pull theidledeveloper/docker-gatling:latest`

Specific version:

`docker pull theidledeveloper/docker-gatling:2.2.5`


# Build the image

Latest version:

`docker build . -t theidledeveloper/docker-gatling`

Specific version:

`docker build . -t theidledeveloper/docker-gatling:2.2.5`


# Usage

Running the container and entering sh

```
docker run -it --rm --entrypoint="/bin/sh" theidledeveloper/docker-gatling
```

Running gatling

```
docker run -it --rm theidledeveloper/docker-gatling
```

Mount configuration and simulation files from host machine

```
docker run --rm \
-v ${pwd}/conf:/opt/gatling/conf \
-v ${pwd}/user-files:/opt/gatling/user-files \
-v ${pwd}/results:/opt/gatling/results \
theidledeveloper/docker-gatling
```

Mount configuration and simulation files from host machine and run a specific simulation

```
docker run --rm \
-v ${pwd}/conf:/opt/gatling/conf \
-v ${pwd}/user-files:/opt/gatling/user-files \
-v ${pwd}/results:/opt/gatling/results \
theidledeveloper/docker-gatling -s basicsimulation
```
