FROM rpi-teamcity_server
LABEL maintainer="uPagge"
LABEL contact_email="upagge@mail.ru"
LABEL telegram="https://t.me/uPagge"

ADD buildAgent.properties TeamCity/buildAgent/conf/

RUN apt-get install -y git

EXPOSE 8111 9090
ENTRYPOINT TeamCity/buildAgent/bin/agent.sh run