# Docker Selenium + NodeJS Image

Docker Image that contains the Selenium Chrome Driver as a node + NodeJS

This image is meant to be within a [Selenium Grid Hub](https://hub.docker.com/r/selenium/hub/), so you can have multiple containers of Selenium Chrome Driver running at the same time.

## Prerequisites

You first need to have a Selenium Grid Hub running:

```
$ docker run -d -p 4444:4444 --name selenium-hub selenium/hub:3.5.3-astatine
```

## Usage

Spawn as many containers as needed:

```
docker run -d --link selenium-hub:hub royestone/selenium-nodejs
```

Note that you link the container to the grid hub with `--link` and the name that you previously set with `--name`
