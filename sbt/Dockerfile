FROM c0d3r/java:latest

MAINTAINER Ivan Fastov c0d3r85@gmail.com

RUN echo "deb https://dl.bintray.com/sbt/debian /" | tee -a /etc/apt/sources.list.d/sbt.list
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 2EE0EA64E40A89B84B2DF73499E82A75642AC823
RUN DEBIAN_FRONTEND=noninteractive apt-get update
RUN DEBIAN_FRONTEND=noninteractive apt-get install sbt -y

RUN sbt info


#ENV HOME=/home/developer
#ARG uid=0
#ARG gid=0
#RUN groupadd -g $gid developer
#RUN useradd -u $uid -g $gid -m developer
#USER developer
#WORKDIR $HOME/project