from centos:latest
MAINTAINER tarrsalah@gmail.com

RUN rpm -Uvh https://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm
RUN rpm -Uvh https://mirror.webtatic.com/yum/el7/webtatic-release.rpm

RUN yum -y update
RUN yum -y upgrade

RUN yum -y install openssl httpd

RUN yum -y install php69w php71w-cli php56w-openid php71w-mysql php71-gd php71-xml php71w-mbstring php71w-openssl

RUN yum -y clean all

WORKDIR /var/www/html

ENTRYPOINT ["/usr/sbin/httpd", "-D", "FOREGROUND"]
