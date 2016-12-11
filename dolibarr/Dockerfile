from centos:latest
MAINTAINER tarrsalah@gmail.com

RUN yum -y update
RUN yum -y upgrade

RUN rpm -Uvh https://mirror.webtatic.com/yum/el7/epel-release.rpm
RUN rpm -Uvh https://mirror.webtatic.com/yum/el7/webtatic-release.rpm

RUN yum -y update && yum clean all

RUN yum -y install httpd

RUN yum -y install php56w php56w-cli php56w-gd php56w-mysql php56-mbsting php56w-gd php56w-pecl-xdebug && yum clean all

COPY ./vhost.conf /etc/httpd/conf.d

ENTRYPOINT ["/usr/sbin/httpd", "-D", "FOREGROUND"]
