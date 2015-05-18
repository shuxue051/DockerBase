# MongoDB
# VERSION  1.0

# use the ubuntu base image provided by dotCloud
FROM ubuntu:latest

# Format: MAINTAINER Name <email@addr.ess>
MAINTAINER Robin <myname@addr.ess>

RUN groupadd -r mongodb && useradd -r -g mongodb mongodb

# Import MongoDB public GPG key AND create a MongoDB list file
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 7F0CEB10
RUN echo 'deb http://downloads-distro.mongodb.org/repo/ubuntu-upstart dist 10gen' | tee /etc/apt/sources.list.d/10gen.list
RUN apt-get update

# install mongodb
RUN apt-get install -y -q mongodb-org

# Create the MongoDB data directory

RUN mkdir -p /data/db && chown -R mongodb:mongodb /data/db
VOLUME /data/db

EXPOSE 27017
ENTRYPOINT ["usr/bin/mongod"]

CMD ["mongod"]
