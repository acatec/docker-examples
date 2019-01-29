
# Nginx

Для запуска контейнера выполним команду:

```
$ docker run -d --name some-nginx -p 85:80 -v $(pwd)/html:/usr/share/nginx/html:ro nginx:latest
```

Проверим результат http://localhost:85/



Теперь то же самое, только через Dockerfile


```Dockerfile
FROM nginx
COPY . /usr/share/nginx/html

EXPOSE 80
```

```bash
$ docker build -t some-content-nginx .
$ docker run --name some-nginx -d -p 85:80 some-content-nginx
```


### Навигация
* [Начало](./../README.MD)
* [Основные команды](./../1_first/README.MD)
* [Mongo](./../3_mongo_dockerfile/MONGO.MD)
* [Wordpress](./../4_wordpress_docker-compose/WORDPRESS.MD)
* [Microsoft](./../5_microsoft/MICROSOFT.MD)