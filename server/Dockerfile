FROM rpi-teamcity_oraclejdk-8
MAINTAINER pixelistik <code@pixelistik.de>

RUN wget -v https://download.jetbrains.com/teamcity/TeamCity-2020.1.4.tar.gz && \
    tar -xzvf TeamCity-2020.1.4.tar.gz && \
    rm TeamCity-2020.1.4.tar.gz

EXPOSE 8111 9090

ENV TEAMCITY_DATA_PATH /root/BuildServer
ENTRYPOINT ["TeamCity/bin/teamcity-server.sh","run"]
