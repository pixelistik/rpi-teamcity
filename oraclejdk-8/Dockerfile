FROM sdhibit/rpi-raspbian
MAINTAINER pixelistik <code@pixelistik.de>
RUN apt-get update
RUN apt-get install -y wget
RUN wget http://archive.raspberrypi.org/debian/raspberrypi.gpg.key -O - | apt-key add -
RUN echo "deb http://archive.raspberrypi.org/debian/ wheezy main" > /etc/apt/sources.list.d/raspberrypi.org.list
RUN apt-get update
RUN apt-get upgrade -y
RUN apt-get install -y oracle-java8-jdk
