FROM mysql:8
LABEL author="João Eduardo Montandon"

ENV MYSQL_ROOT_PASSWORD root
ADD store.sql /docker-entrypoint-initdb.d

EXPOSE 3306
