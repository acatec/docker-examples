
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