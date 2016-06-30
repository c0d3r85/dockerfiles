FROM c0d3r/sbt:latest

MAINTAINER Ivan Fastov c0d3r85@gmail.com

RUN apt-get install libgtk2.0-0 libxtst6 -y

ADD http://downloads.typesafe.com/scalaide-pack/4.4.1-vfinal-luna-211-20160504/scala-SDK-4.4.1-vfinal-2.11-linux.gtk.x86_64.tar.gz /tmp/scala-ide.tar.gz

ENV HOME=/home/developer
ARG uid=0
ARG gid=0
RUN groupadd -g $gid developer
RUN useradd -u $uid -g $gid -m developer
RUN chown developer:developer /tmp/scala-ide.tar.gz

WORKDIR $HOME
USER developer
RUN tar -xzf /tmp/scala-ide.tar.gz

# Cleanup
RUN rm /tmp/scala-ide.tar.gz
