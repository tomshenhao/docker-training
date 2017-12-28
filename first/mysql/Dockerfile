#
# MAINTAINER        Tom.Shen <t.shenhao@gmail.com>
# DOCKER-VERSION    17.12
#
# Dockerizing Mariadb: Dockerfile for building Mariadb images
#
FROM tom/centos:7.4
MAINTAINER Tom.Shen <t.shenhao@gmail.com>

ENV DATA_DIR /var/lib/mysql

# Install Mariadb
RUN yum install -y mariadb mariadb-server && \
    yum clean all

ADD mysqld_charset.cnf /etc/my.cnf.d/

COPY scripts /scripts
RUN chmod +x /scripts/start
RUN chmod +x /scripts/firstrun_maria

EXPOSE 3306

VOLUME ["/var/lib/mysql"]

ENTRYPOINT ["/scripts/start"]
