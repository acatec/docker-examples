Запустим первый контейнер:

```
$ docker run ubuntu:16.04 /bin/echo 'Hello world'
```

```
$ docker run --rm ubuntu:16.04 /bin/echo 'Hello world'

# --rm    Автоматически удаляет контейнер после завершения процесса
```

```
# Список работающих контейнеров
$ docker ps
```

```
# Список всех контейнеров
$ docker ps -a
```


```
# Запустим контейнер в режиме демона
# флаг -d запускает контейнер в фоновом режиме
$ docker run --name daemon -d ubuntu:16.04 /bin/sh -c "while true; do echo hello world; sleep 1; done"
```

```

# Посмотрим логи
$ docker logs -f daemon
```

```
# Можем зайти внутрь контейнера
$ docker exec -it daemon bash
```

```
# Останавливаем
$ docker stop daemon
```

```
# Запускаем
$ docker start daemon
```

```
# Удаляем контейнер
$ docker rm daemon
```

```
# Развернутая информация о контейнере
$ docker inspect daemon
```

```
# Список образов
$ docker images
```

### Навигация
* [Начало](./../README.MD)
* [Nginx](./../2_nginx/NGINX.MD)
* [Mongo](./../3_mongo_dockerfile/MONGO.MD)
* [Wordpress](./../4_wordpress_docker-compose/WORDPRESS.MD)
* [Microsoft](./../5_microsoft/MICROSOFT.MD)
