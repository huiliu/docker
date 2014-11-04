FROM centos:centos6
MAINTAINER Liu Hui <liuhui@viivgame.cn>

RUN useradd core
RUN yum install -y php-fpm php-gd php-mbstring php-mysql php-mcrpy php-imap
RUN rm -f /etc/php-fpm.d/www.conf
ADD config /config
ADD etc /etc

ENTRYPOINT ["/bin/sh", "/config/init"]
#ENTRYPOINT ["/usr/bin/php-fpm", "-F"]
