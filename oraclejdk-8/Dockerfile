FROM sdhibit/rpi-raspbian
MAINTAINER pixelistik <code@pixelistik.de>

# https://gist.github.com/jpetazzo/6127116
RUN echo "force-unsafe-io" > /etc/dpkg/dpkg.cfg.d/02apt-speedup && \
    echo "Acquire::http {No-Cache=True;};" > /etc/apt/apt.conf.d/no-cache

RUN apt-get update && \
    apt-get install -y -q wget ca-certificates && \
    wget http://archive.raspberrypi.org/debian/raspberrypi.gpg.key -O - | apt-key add - && \
    echo "deb http://archive.raspberrypi.org/debian/ wheezy main" > /etc/apt/sources.list.d/raspberrypi.org.list
RUN apt-get update && \
    apt-get upgrade -y

RUN apt-get install -y oracle-java8-jdk
