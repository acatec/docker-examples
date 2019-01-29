Запустим первый контейнер:

```shell
$ docker run ubuntu:16.04 /bin/echo 'Hello world'
```

```shell
$ docker run --rm ubuntu:16.04 /bin/echo 'Hello world'

# --rm    Автоматически удаляет контейнер после завершения процесса
```

```shell
# Список работающих контейнеров
$ docker ps
```

```shell
# Список всех контейнеров
$ docker ps -a
```


```shell
# Запустим контейнер в режиме демона
# флаг -d запускает контейнер в фоновом режиме
$ docker run --name daemon -d ubuntu:16.04 /bin/sh -c "while true; do echo hello world; sleep 1; done"
```

```shell
# Посмотрим логи
$ docker logs -f daemon
```

```shell
# Можем зайти внутрь контейнера
$ docker exec -it daemon bash
```

```shell
# Останавливаем
$ docker stop daemon
```

```shell
# Запускаем
$ docker start daemon
```

```shell
# Удаляем контейнер
$ docker rm daemon
```

```shell
# Развернутая информация о контейнере
$ docker inspect daemon
```

```shell
# Список образов
$ docker images
```

### Навигация
* [Начало](./../README.MD)
* [Nginx](./../2_nginx/NGINX.MD)
* [Mongo](./../3_mongo_dockerfile/MONGO.MD)
* [Wordpress](./../4_wordpress_docker-compose/WORDPRESS.MD)
* [Microsoft](./../5_microsoft/MICROSOFT.MD)
