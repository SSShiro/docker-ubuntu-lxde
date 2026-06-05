# docker-ubuntu-lxde

[![Docker Pulls](https://img.shields.io/docker/pulls/ssshiro/docker-ubuntu-lxde?style=for-the-badge)](https://hub.docker.com/r/ssshiro/docker-ubuntu-lxde)
[![GitHub](https://img.shields.io/github/license/SSShiro/docker-ubuntu-lxde?style=for-the-badge)](https://github.com/SSShiro/docker-ubuntu-lxde)

[![GitHub Workflow Status (with event)](https://img.shields.io/github/actions/workflow/status/SSShiro/docker-ubuntu-lxde/.github%2Fworkflows%2Fubuntu20.04_all.yml?logo=githubactions&label=Build%20Ubuntu20.04%20based%20Docker%20images&style=for-the-badge)](https://github.com/SSShiro/docker-ubuntu-lxde/actions/workflows/ubuntu20.04_all.yml)
[![GitHub Workflow Status (with event)](https://img.shields.io/github/actions/workflow/status/SSShiro/docker-ubuntu-lxde/.github%2Fworkflows%2Fubuntu22.04_all.yml?logo=githubactions&label=Build%20Ubuntu22.04%20based%20Docker%20images&style=for-the-badge)](https://github.com/SSShiro/docker-ubuntu-lxde/actions/workflows/ubuntu22.04_all.yml)
[![GitHub Workflow Status (with event)](https://img.shields.io/github/actions/workflow/status/SSShiro/docker-ubuntu-lxde/.github%2Fworkflows%2Fubuntu24.04_all.yml?logo=githubactions&label=Build%20Ubuntu24.04%20based%20Docker%20images&style=for-the-badge)](https://github.com/SSShiro/docker-ubuntu-lxde/actions/workflows/ubuntu24.04_all.yml)

## Быстрый старт

- [README | XRDP Docker образ](https://github.com/SSShiro/docker-ubuntu-lxde/blob/master/xrdp/README.md)
- [README | VNC/noVNC Docker образ](https://github.com/SSShiro/docker-ubuntu-lxde/blob/master/vnc/README.md)

## Что это?

Docker-образы с рабочим столом LXDE/LXQt на базе Ubuntu.
Для удалённого подключения используются RDP (xrdp) и VNC (x11vnc, noVNC).

Русская локаль, часовой пояс Moscow. При запуске от обычного пользователя через `-u` доступна команда `sudo`.

## Поддерживаемые теги

### XRDP

- [![Docker Image Size (tag)](https://img.shields.io/docker/image-size/ssshiro/docker-ubuntu-lxde/24.04-xrdp_ru?style=flat-square)](https://hub.docker.com/r/ssshiro/docker-ubuntu-lxde/tags?name=24.04-xrdp_ru)
  `24.04-xrdp_ru`, `noble-xrdp_ru`, `latest-xrdp`, `latest`: Ubuntu 24.04, LXQt [(xrdp/Dockerfile.ubuntu24.04)](https://github.com/SSShiro/docker-ubuntu-lxde/blob/master/xrdp/Dockerfile.ubuntu24.04)
- [![Docker Image Size (tag)](https://img.shields.io/docker/image-size/ssshiro/docker-ubuntu-lxde/24.04-xrdp-slim_ru?style=flat-square)](https://hub.docker.com/r/ssshiro/docker-ubuntu-lxde/tags?name=24.04-xrdp-slim_ru)
  `24.04-xrdp-slim_ru`, `noble-xrdp-slim_ru`: облегчённый Ubuntu 24.04, LXQt [(xrdp/Dockerfile.ubuntu24.04)](https://github.com/SSShiro/docker-ubuntu-lxde/blob/master/xrdp/Dockerfile.ubuntu24.04)
- [![Docker Image Size (tag)](https://img.shields.io/docker/image-size/ssshiro/docker-ubuntu-lxde/24.04-xrdp-audio_ru?style=flat-square)](https://hub.docker.com/r/ssshiro/docker-ubuntu-lxde/tags?name=24.04-xrdp-audio_ru)
  `24.04-xrdp-audio_ru`, `noble-xrdp-audio_ru`: Ubuntu 24.04, LXQt с поддержкой звука [(xrdp/Dockerfile.ubuntu24.04_audio)](https://github.com/SSShiro/docker-ubuntu-lxde/blob/master/xrdp/Dockerfile.ubuntu24.04_audio)
- [![Docker Image Size (tag)](https://img.shields.io/docker/image-size/ssshiro/docker-ubuntu-lxde/22.04-xrdp_ru?style=flat-square)](https://hub.docker.com/r/ssshiro/docker-ubuntu-lxde/tags?name=22.04-xrdp_ru)
  `22.04-xrdp_ru`, `jammy-xrdp_ru`: Ubuntu 22.04, LXDE [(xrdp/Dockerfile.ubuntu22.04)](https://github.com/SSShiro/docker-ubuntu-lxde/blob/master/xrdp/Dockerfile.ubuntu22.04)
- [![Docker Image Size (tag)](https://img.shields.io/docker/image-size/ssshiro/docker-ubuntu-lxde/22.04-xrdp-slim_ru?style=flat-square)](https://hub.docker.com/r/ssshiro/docker-ubuntu-lxde/tags?name=22.04-xrdp-slim_ru)
  `22.04-xrdp-slim_ru`, `jammy-xrdp-slim_ru`: облегчённый Ubuntu 22.04, LXDE [(xrdp/Dockerfile.ubuntu22.04)](https://github.com/SSShiro/docker-ubuntu-lxde/blob/master/xrdp/Dockerfile.ubuntu22.04)
- [![Docker Image Size (tag)](https://img.shields.io/docker/image-size/ssshiro/docker-ubuntu-lxde/22.04-xrdp-pulseaudio_ru?style=flat-square)](https://hub.docker.com/r/ssshiro/docker-ubuntu-lxde/tags?name=22.04-xrdp-pulseaudio_ru)
  `22.04-xrdp-pulseaudio_ru`, `jammy-xrdp-pulseaudio_ru`: Ubuntu 22.04, LXDE с поддержкой звука [(xrdp/Dockerfile.ubuntu22.04_pulseaudio)](https://github.com/SSShiro/docker-ubuntu-lxde/blob/master/xrdp/Dockerfile.ubuntu22.04_pulseaudio)
- [![Docker Image Size (tag)](https://img.shields.io/docker/image-size/ssshiro/docker-ubuntu-lxde/20.04-xrdp_ru?style=flat-square)](https://hub.docker.com/r/ssshiro/docker-ubuntu-lxde/tags?name=20.04-xrdp_ru)
  `20.04-xrdp_ru`, `focal-xrdp_ru`: Ubuntu 20.04, LXDE [(xrdp/Dockerfile.ubuntu20.04)](https://github.com/SSShiro/docker-ubuntu-lxde/blob/master/xrdp/Dockerfile.ubuntu20.04)
- [![Docker Image Size (tag)](https://img.shields.io/docker/image-size/ssshiro/docker-ubuntu-lxde/20.04-xrdp-slim_ru?style=flat-square)](https://hub.docker.com/r/ssshiro/docker-ubuntu-lxde/tags?name=20.04-xrdp-slim_ru)
  `20.04-xrdp-slim_ru`, `focal-xrdp-slim_ru`: облегчённый Ubuntu 20.04, LXDE [(xrdp/Dockerfile.ubuntu20.04)](https://github.com/SSShiro/docker-ubuntu-lxde/blob/master/xrdp/Dockerfile.ubuntu20.04)
- [![Docker Image Size (tag)](https://img.shields.io/docker/image-size/ssshiro/docker-ubuntu-lxde/20.04-xrdp-pulseaudio_ru?style=flat-square)](https://hub.docker.com/r/ssshiro/docker-ubuntu-lxde/tags?name=20.04-xrdp-pulseaudio_ru)
  `20.04-xrdp-pulseaudio_ru`, `focal-xrdp-pulseaudio_ru`: Ubuntu 20.04, LXDE с поддержкой звука [(xrdp/Dockerfile.ubuntu20.04_pulseaudio)](https://github.com/SSShiro/docker-ubuntu-lxde/blob/master/xrdp/Dockerfile.ubuntu20.04_pulseaudio)

### VNC

- [![Docker Image Size (tag)](https://img.shields.io/docker/image-size/ssshiro/docker-ubuntu-lxde/24.04-vnc_ru?style=flat-square)](https://hub.docker.com/r/ssshiro/docker-ubuntu-lxde/tags?name=24.04-vnc_ru)
  `24.04-vnc_ru`, `noble-vnc_ru`, `latest-vnc`: Ubuntu 24.04, LXQt [(vnc/Dockerfile.ubuntu24.04)](https://github.com/SSShiro/docker-ubuntu-lxde/blob/master/vnc/Dockerfile.ubuntu24.04)
- [![Docker Image Size (tag)](https://img.shields.io/docker/image-size/ssshiro/docker-ubuntu-lxde/24.04-vnc-slim_ru?style=flat-square)](https://hub.docker.com/r/ssshiro/docker-ubuntu-lxde/tags?name=24.04-vnc-slim_ru)
  `24.04-vnc-slim_ru`, `noble-vnc-slim_ru`: облегчённый Ubuntu 24.04, LXQt [(vnc/Dockerfile.ubuntu24.04)](https://github.com/SSShiro/docker-ubuntu-lxde/blob/master/vnc/Dockerfile.ubuntu24.04)
- [![Docker Image Size (tag)](https://img.shields.io/docker/image-size/ssshiro/docker-ubuntu-lxde/22.04-vnc_ru?style=flat-square)](https://hub.docker.com/r/ssshiro/docker-ubuntu-lxde/tags?name=22.04-vnc_ru)
  `22.04-vnc_ru`, `jammy-vnc_ru`: Ubuntu 22.04, LXDE [(vnc/Dockerfile.ubuntu22.04)](https://github.com/SSShiro/docker-ubuntu-lxde/blob/master/vnc/Dockerfile.ubuntu22.04)
- [![Docker Image Size (tag)](https://img.shields.io/docker/image-size/ssshiro/docker-ubuntu-lxde/22.04-vnc-slim_ru?style=flat-square)](https://hub.docker.com/r/ssshiro/docker-ubuntu-lxde/tags?name=22.04-vnc-slim_ru)
  `22.04-vnc-slim_ru`, `jammy-vnc-slim_ru`: облегчённый Ubuntu 22.04, LXDE [(vnc/Dockerfile.ubuntu22.04)](https://github.com/SSShiro/docker-ubuntu-lxde/blob/master/vnc/Dockerfile.ubuntu22.04)
- [![Docker Image Size (tag)](https://img.shields.io/docker/image-size/ssshiro/docker-ubuntu-lxde/20.04-vnc_ru?style=flat-square)](https://hub.docker.com/r/ssshiro/docker-ubuntu-lxde/tags?name=20.04-vnc_ru)
  `20.04-vnc_ru`, `focal-vnc_ru`: Ubuntu 20.04, LXDE [(vnc/Dockerfile.ubuntu20.04)](https://github.com/SSShiro/docker-ubuntu-lxde/blob/master/vnc/Dockerfile.ubuntu20.04)
- [![Docker Image Size (tag)](https://img.shields.io/docker/image-size/ssshiro/docker-ubuntu-lxde/20.04-vnc-slim_ru?style=flat-square)](https://hub.docker.com/r/ssshiro/docker-ubuntu-lxde/tags?name=20.04-vnc-slim_ru)
  `20.04-vnc-slim_ru`, `focal-vnc-slim_ru`: облегчённый Ubuntu 20.04, LXDE [(vnc/Dockerfile.ubuntu20.04)](https://github.com/SSShiro/docker-ubuntu-lxde/blob/master/vnc/Dockerfile.ubuntu20.04)

## Быстрый запуск

### XRDP

```sh
$ docker run -it \
    -p 3389:3389 \
    -u $(id -u):$(id -g) \
    -e USER=developer \
    -e PASSWD=mypasswd \
    ssshiro/docker-ubuntu-lxde:24.04-xrdp_ru
```

Подключитесь через приложение удалённого рабочего стола к `<IP-адрес Docker-хоста>:3389`.
Имя пользователя — `developer`, пароль — `mypasswd`.

Если после подключения не отображается экран входа или рабочий стол, попробуйте добавить опцию `--privileged`.

Подробное описание параметров см. в [README | XRDP Docker образ](https://github.com/SSShiro/docker-ubuntu-lxde/blob/master/xrdp/README.md).

### VNC

```sh
$ docker run -it \
    -p 5900:5900 \
    -p 8080:80 \
    -u $(id -u):$(id -g) \
    -e USER=developer \
    -e PASSWD=mypasswd \
    -e RESOLUTION=1024x768x24 \
    ssshiro/docker-ubuntu-lxde:24.04-vnc_ru
```

Подключитесь VNC-клиентом (VNC Viewer) к `<IP-адрес Docker-хоста>:5900`.
Или откройте в браузере `http://<IP-адрес Docker-хоста>:8080/vnc.html`.
Пароль — `mypasswd`.

Если после подключения не отображается рабочий стол, попробуйте добавить опцию `--privileged`.

Подробное описание параметров см. в [README | VNC/noVNC Docker образ](https://github.com/SSShiro/docker-ubuntu-lxde/blob/master/vnc/README.md).

## Скриншоты

### XRDP

![Скриншот XRDP](https://raw.githubusercontent.com/SSShiro/docker-ubuntu-lxde/master/screenshot/XRDP-ubuntu24.04_ja.png)

### VNC

![Скриншот VNC](https://raw.githubusercontent.com/SSShiro/docker-ubuntu-lxde/master/screenshot/VNC-ubuntu24.04_ja.png)

### noVNC

![Скриншот noVNC](https://raw.githubusercontent.com/SSShiro/docker-ubuntu-lxde/master/screenshot/noVNC-ubuntu24.04_ja.png)
