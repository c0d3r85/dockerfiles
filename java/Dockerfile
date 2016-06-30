FROM ubuntu:16.04

MAINTAINER Ivan Fastov c0d3r85@gmail.com

RUN DEBIAN_FRONTEND=noninteractive apt-get update

RUN DEBIAN_FRONTEND=noninteractive apt-get install software-properties-common apt-transport-https -y

RUN add-apt-repository ppa:webupd8team/java

RUN DEBIAN_FRONTEND=noninteractive apt-get update
RUN DEBIAN_FRONTEND=noninteractive apt-get upgrade --with-new-pkgs -y

RUN echo oracle-java8-installer shared/accepted-oracle-license-v1-1 select true | /usr/bin/debconf-set-selections
RUN DEBIAN_FRONTEND=noninteractive apt-get install oracle-java8-installer oracle-java8-set-default -y
