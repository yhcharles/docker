FROM dockerfile/nodejs
MAINTAINER John E. Arnold, iohannes.eduardus.arnold@gmail.com

# Get Etherpad-lite's other dependencies
RUN apt-get update
RUN apt-get install -y gzip git-core curl python libssl-dev pkg-config build-essential supervisor

# Grab the latest Git version
RUN cd /opt && git clone git://github.com/ether/etherpad-lite.git etherpad

# Install node dependencies
RUN /opt/etherpad/bin/installDeps.sh

# Add conf files
ADD settings.json /opt/etherpad/settings.json
ADD supervisor.conf /etc/supervisor/supervisor.conf

EXPOSE 80
CMD ["supervisord", "-c", "/etc/supervisor/supervisor.conf", "-n"]
