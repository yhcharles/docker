# Version: 0.0.1
FROM debian:jessie
MAINTAINER charlieyan

RUN apt-get update

# install ssh service
# turn on port 36000
# set password
RUN apt-get install -y openssh-server
RUN mkdir -p /var/run/sshd
RUN sed -i "s/PermitRootLogin without-password/PermitRootLogin yes/" /etc/ssh/sshd_config
RUN sed -i "s/UsePrivilegeSeparation.*/UsePrivilegeSeparation no/g" /etc/ssh/sshd_config
RUN sed -i "s/Port 22/Port 36000/" /etc/ssh/sshd_config
RUN echo "root:root" | chpasswd

RUN apt-get install -y vim
RUN apt-get install -y gawk
RUN apt-get install -y default-jdk

RUN apt-get install -y python
RUN apt-get install -y python-pip
RUN apt-get install -y python-protobuf
RUN pip install gearman
RUN pip install ipython
RUN pip install numpy scipy scikit-learn

EXPOSE 36000
CMD ["/usr/sbin/sshd", "-D"]

