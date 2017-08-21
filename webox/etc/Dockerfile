from centos:latest
MAINTAINER tarrsalah@gmail.com

RUN rpm -Uvh https://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm
RUN rpm -Uvh https://mirror.webtatic.com/yum/el7/webtatic-release.rpm

RUN yum -y update
RUN yum -y upgrade

RUN yum -y install httpd openssl php71w php71w-cli php71-mbstring php71-mysqlnd php71-pdo
RUN yum clean all

ADD ./apache.conf /etc/httpd/conf.d

WORKDIR /var/www/html

ENTRYPOINT ["/usr/sbin/httpd", "-D", "FOREGROUND"]
