from centos:latest
MAINTAINER tarrsalah@gmail.com

RUN rpm -Uvh https://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm
RUN rpm -Uvh https://mirror.webtatic.com/yum/el7/webtatic-release.rpm

RUN yum -y update
RUN yum -y upgrade

RUN yum -y install php71w php71w-cli php71w-mysqlnd php71w-gd php71w-mbstring php71w-dom httpd

RUN yum clean all

RUN php -r "readfile('https://getcomposer.org/installer');" | php && mv composer.phar /usr/local/bin/composer

ENV PATH "$PATH:/usr/local/bin"

RUN composer global require drush/drush
ENV PATH "$PATH:/root/.composer/vendor/bin"


COPY ./vhost.conf /etc/httpd/conf.d

WORKDIR /var/www/html

ENTRYPOINT ["/usr/sbin/httpd", "-D", "FOREGROUND"]
