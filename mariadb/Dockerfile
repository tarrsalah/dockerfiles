FROM mariadb:10.2.14

ENV MYSQL_ROOT_PASSWORD root
ENV MYSQL_DATABASE db
ENV MYSQL_USER admin
ENV MYSQL_PASSWORD admin

CMD ["mysqld", "--character-set-server=utf8mb4", "--collation-server=utf8mb4_unicode_ci", "--sql_mode=''"]
