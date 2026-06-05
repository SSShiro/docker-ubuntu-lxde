# docker-ubuntu-lxde VNC

[![Docker Pulls](https://img.shields.io/docker/pulls/ssshiro/docker-ubuntu-lxde?style=for-the-badge)](https://hub.docker.com/r/ssshiro/docker-ubuntu-lxde)
[![GitHub](https://img.shields.io/github/license/SSShiro/docker-ubuntu-lxde?style=for-the-badge)](https://github.com/SSShiro/docker-ubuntu-lxde)

## Что это?

Docker-образ с рабочим столом LXDE/LXQt на базе Ubuntu.
Для удалённого подключения используется VNC (x11vnc, noVNC).

Русская локаль, часовой пояс Moscow. При запуске от обычного пользователя через `-u` доступна команда `sudo`.

![Скриншот VNC](https://raw.githubusercontent.com/SSShiro/docker-ubuntu-lxde/master/screenshot/VNC-ubuntu24.04_ja.png)
![Скриншот noVNC](https://raw.githubusercontent.com/SSShiro/docker-ubuntu-lxde/master/screenshot/noVNC-ubuntu24.04_ja.png)

## Поддерживаемые теги

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

## Использование

### Запуск контейнера

```
$ docker run --rm -it \
    -p 5900:5900 \
    -p 8080:80 \
    -u $(id -u):$(id -g) \
    -e USER=developer \
    -e PASSWD=mypasswd \
    -e RESOLUTION=1024x768x24 \
    ssshiro/docker-ubuntu-lxde:24.04-vnc_ru
```

Параметры запуска:

- `-p vnc_port:5900`
  Укажите в `vnc_port` порт для подключения VNC-клиента.
  Не требуется, если VNC-клиент не используется (только noVNC).
- `-p novnc_port:80`
  Укажите в `novnc_port` порт для подключения через браузер.
  Не требуется, если noVNC не используется (только VNC-клиент).
- `-u user:group`
  Укажите UID в `user` и GID в `group` для запуска контейнера.
  Если не задано — контейнер запускается от root (UID=0, GID=0).
- `-e USER=loginUser`
  Имя пользователя для входа в рабочий стол. По умолчанию — `developer`
  (при запуске от root — `root`).
- `-e PASSWD=loginPasswd`
  Пароль для входа. По умолчанию — `vncpasswd`.
- `-e RESOLUTION=WxHxD`
  Разрешение экрана: ширина `W`, высота `H`, глубина цвета `D`.
  По умолчанию — `1280x720x24`.

Если после подключения не отображается рабочий стол, попробуйте добавить опцию `--privileged`.

Большинство пользовательских настроек хранятся в домашнем каталоге контейнера.
Чтобы сохранять их между перезапусками, добавьте `-v ${HOME}/container_home:/home/developer`.
**Создайте каталог для монтирования заранее**, иначе возникнет ошибка прав доступа.

### Подключение клиента

#### VNC-клиент

После `docker run` подключитесь через VNC-клиент (RealVNC, UltraVNC и др.).

Адрес подключения: `<IP Docker-хоста>:<vnc_port>`, пароль — значение `-e PASSWD`.

#### noVNC

После `docker run` откройте в браузере:

`http://<IP Docker-хоста>:<novnc_port>/vnc.html` (например, `http://localhost:8080/vnc.html`)

Пароль — значение `-e PASSWD`.

## Сборка образа

```
$ git clone https://github.com/SSShiro/docker-ubuntu-lxde.git
$ docker build \
    -t lxde_vnc:ubuntu24.04_ru \
    -f ./vnc/Dockerfile.ubuntu24.04 \
    ./vnc
```
