# docker-ubuntu-lxde XRDP

[![Docker Pulls](https://img.shields.io/docker/pulls/ssshiro/docker-ubuntu-lxde?style=for-the-badge)](https://hub.docker.com/r/ssshiro/docker-ubuntu-lxde)
[![GitHub](https://img.shields.io/github/license/SSShiro/docker-ubuntu-lxde?style=for-the-badge)](https://github.com/SSShiro/docker-ubuntu-lxde)

## Что это?

Docker-образ с рабочим столом LXDE/LXQt на базе Ubuntu.
Для удалённого подключения используется RDP (xrdp).

Русская локаль, часовой пояс Moscow. При запуске от обычного пользователя через `-u` доступна команда `sudo`.

![Скриншот XRDP](https://raw.githubusercontent.com/SSShiro/docker-ubuntu-lxde/master/screenshot/XRDP-ubuntu24.04_ja.png)

## Поддерживаемые теги

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
- ![Static Badge](https://img.shields.io/badge/EOL-darkred?style=flat-square)
  `ubuntu18.04_ru`: Ubuntu 18.04 (EOL) [(xrdp/Dockerfile.ubuntu18.04)](https://github.com/SSShiro/docker-ubuntu-lxde/blob/master/xrdp/Dockerfile.ubuntu18.04)
- ![Static Badge](https://img.shields.io/badge/EOL-darkred?style=flat-square)
  `ubuntu18.04-pulseaudio_ru`: Ubuntu 18.04 с поддержкой звука (EOL) [(xrdp/Dockerfile.ubuntu18.04_pulseaudio)](https://github.com/SSShiro/docker-ubuntu-lxde/blob/master/xrdp/Dockerfile.ubuntu18.04_pulseaudio)
- ![Static Badge](https://img.shields.io/badge/EOL-darkred?style=flat-square)
  `ubuntu16.04_ru`: Ubuntu 16.04 (EOL) [(xrdp/Dockerfile.ubuntu16.04)](https://github.com/SSShiro/docker-ubuntu-lxde/blob/master/xrdp/Dockerfile.ubuntu16.04)

## Использование

### Запуск контейнера

```
$ docker run --rm -it \
    -p 3389:3389 \
    -u $(id -u):$(id -g) \
    -e USER=developer \
    -e PASSWD=mypasswd \
    ssshiro/docker-ubuntu-lxde:24.04-xrdp_ru
```

Параметры запуска:

- `-p port:3389`
  Укажите в `port` порт для подключения клиента.
- `-u user:group`
  Укажите UID в `user` и GID в `group` для запуска контейнера.
  Если не задано — контейнер запускается от root (UID=0, GID=0).
- `-e USER=loginUser`
  Имя пользователя для входа через RDP. По умолчанию — `developer`
  (при запуске от root — `root`).
- `-e PASSWD=loginPasswd`
  Пароль для входа через RDP. По умолчанию — `xrdppasswd`.

Если после подключения не отображается экран входа или рабочий стол, попробуйте добавить опцию `--privileged`.

Большинство пользовательских настроек хранятся в домашнем каталоге контейнера.
Чтобы сохранять их между перезапусками, добавьте `-v ${HOME}/container_home:/home/developer`.
**Создайте каталог для монтирования заранее**, иначе возникнет ошибка прав доступа.

### Подключение клиента

После `docker run` подключитесь через приложение удалённого рабочего стола
(Windows — «Подключение к удалённому рабочему столу», macOS — «Microsoft Remote Desktop», Linux — `xfreerdp` или `Remmina`).

Адрес подключения: `<IP Docker-хоста>:<port>`, пользователь — значение `-e USER`, пароль — значение `-e PASSWD`.

### Кастомизация

Этот образ содержит минимальный набор пакетов. Для расширения функциональности рекомендуется создать собственный Dockerfile на его основе или использовать опубликованный образ с Docker Hub как базовый.

Пример кастомизированного образа доступен [здесь](https://github.com/SSShiro/docker-ubuntu-lxde/blob/master/xrdp/examples/ubuntu22.04).

![Пример кастомизации](https://raw.githubusercontent.com/SSShiro/docker-ubuntu-lxde/master/screenshot/XRDP-example-22.04-app.png)

## Сборка образа

```
$ git clone https://github.com/SSShiro/docker-ubuntu-lxde.git
$ docker build \
    -t lxde_xrdp:ubuntu24.04_ru \
    -f ./xrdp/Dockerfile.ubuntu24.04 \
    ./xrdp

## Облегчённый образ
$ docker build \
    --build-arg ADDITIONAL_APT_GET_OPTS=--no-install-recommends \
    -t lxde_xrdp:ubuntu24.04-slim_ru \
    -f ./xrdp/Dockerfile.ubuntu24.04 \
    ./xrdp
```
