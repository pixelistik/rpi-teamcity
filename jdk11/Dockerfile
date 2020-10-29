FROM schachr/raspbian-stretch
LABEL maintainer="Vova Lantsov"
LABEL contact_email="contact@vova-lantsov.dev"
LABEL telegram="https://t.me/vova_lantsov"

# https://gist.github.com/jpetazzo/6127116
RUN echo "force-unsafe-io" > /etc/dpkg/dpkg.cfg.d/02apt-speedup && \
    echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/no-lang

RUN apt-get update && \
    apt-get install -y -q wget ca-certificates && \
    wget http://archive.raspberrypi.org/debian/raspberrypi.gpg.key -O - | apt-key add - && \
    echo "deb http://archive.raspberrypi.org/debian/ wheezy main" > /etc/apt/sources.list.d/raspberrypi.org.list
RUN apt-get update && \
    apt-get upgrade -y

RUN apt-get install -y default-jdk
ENV JAVA_HOME /usr/lib/jvm/java-11-openjdk-amd64