FROM oraclejdk-8
MAINTAINER pixelistik <code@pixelistik.de>
RUN apt-get install -y wget ca-certificates
RUN wget -v https://download.jetbrains.com/teamcity/TeamCity-9.0.3.tar.gz
RUN tar -xzvf TeamCity-9.0.3.tar.gz
EXPOSE 8111
EXPOSE 9090
ENV TEAMCITY_DATA_PATH /root/BuildServer
ENTRYPOINT ["TeamCity/bin/teamcity-server.sh","run"]
