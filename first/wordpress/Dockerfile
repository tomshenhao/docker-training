FROM tom/php-fpm:1.0

ADD init.sh /init.sh
RUN chmod +x /init.sh

ENTRYPOINT ["/init.sh", "/usr/bin/supervisord", "-n", "-c", "/etc/supervisord.conf"]
