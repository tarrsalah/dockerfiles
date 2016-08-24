from centos:latest
MAINTAINER tarrsalah@gmail.com

RUN yum -y update
RUN yum -y upgrade

RUN rpm -Uvh https://mirror.webtatic.com/yum/el7/epel-release.rpm
RUN rpm -Uvh https://mirror.webtatic.com/yum/el7/webtatic-release.rpm

RUN yum -y update && yum clean all

RUN yum -y install httpd

RUN yum -y install php56w php56w-cli php56w-mysql php56w-gd php56w-xml php56w-mbstring && yum clean all

RUN echo "ServerName localhost" >> /etc/httpd/conf/httpd.conf

ENTRYPOINT ["/usr/sbin/httpd", "-D", "FOREGROUND"]
