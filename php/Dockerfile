# Sử dụng image chứa PHP 8.3 trên Alpine Linux
FROM shinsenter/php-archives:20240804-8.3-fpm-alpine

# Cài đặt các công cụ bổ sung
RUN apk add --no-cache \
    supervisor

# Cài đặt WP-CLI
RUN curl -o /usr/local/bin/wp https://raw.githubusercontent.com/wp-cli/builds/gh-pages/phar/wp-cli.phar && \
    chmod +x /usr/local/bin/wp

# Sao chép file supervisord.conf vào container
COPY supervisord.conf /etc/supervisor/conf.d/supervisord.conf

# Lệnh CMD để khởi động supervisord khi container chạy
CMD ["/usr/bin/supervisord", "-c", "/etc/supervisor/conf.d/supervisord.conf"]

# Mở cổng mặc định cho PHP-FPM
EXPOSE 9000