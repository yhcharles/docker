# Version: 0.0.1
FROM debian:jessie
MAINTAINER charlieyan

RUN apt-get update
RUN apt-get install -y python
RUN apt-get install -y python-pip
RUN apt-get install -y python-protobuf
RUN pip install gearman
RUN pip install sh

RUN apt-get install -y gawk
RUN apt-get install -y openssh-server
