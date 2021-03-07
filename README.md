# Gitea on Raspberry Pi
This image hosts [Gitea](https://gitea.io) in a Raspberry Pi docker image of minimal size, yet fully functional.

This work is a fork of [kapdap/gitea-rpi](https://hub.docker.com/r/kapdap/gitea-rpi), but with a slightly smaller image.

## Tags
|Tag Style|Meaning|
|--|--|
|latest|currently 1.13.4

## comments 
* In 1.13.1 the call of external renderers like plantuml doesn't work => rollback doesn't come easy as the downgrading of the database is not supported.
[ticket](https://github.com/go-gitea/gitea/issues/14219)

## Usage
```bash
docker volume create gitea_data
docker run -d -p 22:22 -p 3000:3000 -v gitea_data:/data sepphod/gitea-raspi
```