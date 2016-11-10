from centos:latest

MAINTAINER tarrsalah@gmail.com

RUN rpm -Uvh https://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm
RUN rpm -Uvh https://mirror.webtatic.com/yum/el7/webtatic-release.rpm

RUN yum -y update
RUN yum -y upgrade

RUN yum -y install php70w httpd
RUN yum clean all


RUN sed -i "s/display_errors = Off/display_errors = On/" /etc/php.ini


WORKDIR /var/www/html

ENTRYPOINT ["/usr/sbin/httpd", "-D", "FOREGROUND"]
