FROM rpi-teamcity_server
LABEL maintainer="uPagge"
LABEL contact_email="upagge@mail.ru"
LABEL telegram="https://t.me/uPagge"

ADD buildAgent.properties TeamCity/buildAgent/conf/

#RUN apt-get update && \
#	apt-get install -y software-properties-common && \
#	apt-get update && \
#	apt-get install -y php5-cli php5-mysql php-pear php5-gd php5-curl php5-xdebug poppler-utils gettext make imagemagick

EXPOSE 8111 9090
ENTRYPOINT TeamCity/buildAgent/bin/agent.sh run