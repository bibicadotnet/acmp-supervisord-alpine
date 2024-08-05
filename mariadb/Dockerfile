# Sử dụng image MariaDB 10.1 trên Alpine Linux
FROM wodby/mariadb:10.11-3.28.3

USER root

RUN apk add --no-cache \
    supervisor

COPY supervisord.conf /etc/supervisor/conf.d/supervisord.conf

USER mysql

EXPOSE 3306

CMD ["/usr/bin/supervisord", "-c", "/etc/supervisor/conf.d/supervisord.conf"]