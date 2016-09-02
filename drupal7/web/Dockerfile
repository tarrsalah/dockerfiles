from centos:latest
MAINTAINER tarrsalah@gmail.com

RUN rpm -Uvh https://mirror.webtatic.com/yum/el7/epel-release.rpm
RUN rpm -Uvh https://mirror.webtatic.com/yum/el7/webtatic-release.rpm

RUN yum -y update
RUN yum -y upgrade

RUN yum -y install which openssl httpd mysql

RUN yum -y install php56w php56w-cli php56w-openid php56w-mysql php56w-gd php56w-xml php56w-mbstring php56w-openssl && yum clean all

RUN yum clean all

RUN php -r "readfile('https://getcomposer.org/installer');" | php && mv composer.phar /usr/local/bin/composer

ENV PATH "$PATH:/usr/local/bin"

RUN composer global require drush/drush
ENV PATH "$PATH:/root/.composer/vendor/bin"

RUN echo "ServerName drupal7.local" >> /etc/httpd/conf/httpd.conf

WORKDIR /var/www/html

ENTRYPOINT ["/usr/sbin/httpd", "-D", "FOREGROUND"]
