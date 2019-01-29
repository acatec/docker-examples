FROM ubuntu:16.04

RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv EA312927
RUN echo "deb http://repo.mongodb.org/apt/ubuntu xenial/mongodb-org/3.2 multiverse" | tee /etc/apt/sources.list.d/mongodb-org-3.2.list

RUN apt-get update
RUN apt-get install -y mongodb-org

# Данные будут потеряны при перезапуске
# RUN mkdir -p /data/db

# нные сохранятся
VOLUME /data/db


EXPOSE 27017

CMD ["/usr/bin/mongod"]


# $ docker build -t "monga:dockerfile" .
# $ docker run -p 27017:27017 -v $(pwd)/data:/data/db/:rw monga:dockerfile



# FROM — устанавливает базовый образ.
# RUN — выполняет команду в контейнере.
# ENV — устанавливает переменную окружения.
# WORKDIR — устанавливает рабочую директорию.
# VOLUME — создает точку монтирования для тома.
# CMD — устанавливает исполняемый файл для контейнера.
