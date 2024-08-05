# Sử dụng image chính thức của Caddy từ Docker Hub
FROM caddy:2.8.4-alpine

# Cài đặt các gói cần thiết
RUN apk add --no-cache \
    supervisor

# Sao chép file supervisord.conf vào container
COPY supervisord.conf /etc/supervisor/conf.d/supervisord.conf

# Lệnh CMD để khởi động supervisord khi container chạy
CMD ["/usr/bin/supervisord", "-c", "/etc/supervisor/conf.d/supervisord.conf"]

EXPOSE 80
EXPOSE 443
EXPOSE 2019