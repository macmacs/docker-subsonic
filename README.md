
This repository contains configuration files for building a 
Docker (http://docker.io) image for the Subsonic media streamer.

## Noteworthy

* Subsonic 6.1.3 (http://www.subsonic.org)

## Build your own image

```shell
$ docker build -t macmacs/docker-subsonic .
```

## Get a pre-built image

A current image is available as a trusted build from the Docker index:

```shell
$ docker pull  macmacs/subsonic
```

The repository page is at
https://index.docker.io/u/cyrilix/subsonic/


## Run a container with this image

```shell
$ docker run \
  --name subsonic \
  -d \
  -p 8080:8080 \
  -volume "/wherever/your/music/is:/opt/music/" \
  -volume "/wherever/your/playlists/are:/opt/playlists/" \
  -volume "/wherever/your/podcasts/are:/opt/podcast/" \
  -volume "/wherever/subsonic/data/should/be:/opt/data/" \
  macmacs/subsonic

```

  
