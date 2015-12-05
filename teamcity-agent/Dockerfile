FROM teamcity_teamcity
MAINTAINER pixelistik <code@pixelistik.de>
ADD buildAgent.properties TeamCity/buildAgent/conf/

RUN apt-get update && \
	apt-get install -y php5-cli php5-mysql php-pear php5-gd php5-curl php5-xdebug poppler-utils gettext make imagemagick
	
RUN pear channel-discover pear.cakephp.org && \
	pear install cakephp/CakePHP_CodeSniffer && \
	phpcs --config-set default_standard CakePHP && \
	phpcs --config-set warning_severity 0

EXPOSE 8111 9090
ENTRYPOINT TeamCity/buildAgent/bin/agent.sh run
