Docker-compose.yml
```
version: '3.3'

services:
  db:
    image: mysql:5.7
    volumes:
      - ./mysql/data:/var/lib/mysql
    restart: always
    environment:
      MYSQL_ROOT_PASSWORD: somewordpress
      MYSQL_DATABASE: wordpress
      MYSQL_USER: wordpress
      MYSQL_PASSWORD: wordpress

  wordpress:
    depends_on:
      - db
    image: wordpress:latest
    ports:
      - "8000:80"
    restart: always
    environment:
      WORDPRESS_DB_HOST: db:3306
      WORDPRESS_DB_USER: wordpress
      WORDPRESS_DB_PASSWORD: wordpress

```
Выполнить
```
$ docker-compose up
```
или в фоне
```
$ docker-compose up -d
```


### Навигация
* [Начало](./../README.MD)
* [Основные команды](./../1_first/README.MD)
* [Nginx](./../2_nginx/NGINX.MD)
* [Mongo](./../3_mongo_dockerfile/MONGO.MD)
* [Microsoft](./../5_microsoft/MICROSOFT.MD)