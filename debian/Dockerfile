# Version: 0.0.1
FROM debian:jessie
MAINTAINER charlieyan "charlieyan@tencent.com"

ENV http_proxy=http://proxy.oa.com:8080
ENV https_proxy=http://proxy.oa.com:8080

RUN apt-get update
RUN apt-get install -y python
RUN apt-get install -y python-pip
RUN apt-get install -y python-protobuf
RUN pip install gearman
RUN pip install sh

RUN apt-get install -y gawk
RUN apt-get install -y openssh-server
