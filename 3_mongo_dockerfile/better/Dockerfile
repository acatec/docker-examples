FROM ubuntu:16.04

RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv EA312927 \
 && echo "deb http://repo.mongodb.org/apt/ubuntu xenial/mongodb-org/3.2 multiverse" | tee /etc/apt/sources.list.d/mongodb-org-3.2.list \

 && apt-get update \
 && apt-get install -y mongodb-org \
 && mkdir -p /data/db

EXPOSE 27017

CMD ["/usr/bin/mongod"]


# $ docker build -t "monga:dockerfile" .
# $ docker run -p 27017:27017 monga:dockerfile
