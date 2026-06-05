# docker-ubuntu-lxde XRDP — пример кастомизации

## Что это?

Пример кастомизации на основе [Docker-образа с Docker Hub](https://hub.docker.com/r/ssshiro/docker-ubuntu-lxde).

- Кастомизация экрана входа
  ![Пример — экран входа](https://raw.githubusercontent.com/SSShiro/docker-ubuntu-lxde/master/screenshot/XRDP-example-22.04-login.png)
- Кастомизация темы рабочего стола
  ![Пример — тема](https://raw.githubusercontent.com/SSShiro/docker-ubuntu-lxde/master/screenshot/XRDP-example-22.04.png)
- Установка приложений
  ![Пример — приложения](https://raw.githubusercontent.com/SSShiro/docker-ubuntu-lxde/master/screenshot/XRDP-example-22.04-app.png)

## Использование

### Сборка образа

При необходимости измените имя образа в `docker-compose.yml` (`image`), затем выполните:

```
$ docker compose build
```

### Запуск контейнера

В `docker-compose.yml` укажите в поле `user` свой «UID:GID».
Настройте логин/пароль, порт и каталог монтирования, затем выполните:

```
$ docker compose up -d
```

Если после подключения не отображается экран входа или рабочий стол, добавьте `privileged: true` в `docker-compose.yml`.
