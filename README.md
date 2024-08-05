# Dockerfile ACMP Supervisord Alpine
Sử dụng Docker Desktop để tạo, hỗ trộ arm64 và amd64
```
docker buildx create --name mybuilder
docker buildx use mybuilder
```
### Caddy v2.8.4 with Supervisord
```
docker buildx build --tag bibica/caddy-supervisord-alpine -o type=image --platform=linux/arm64,linux/amd64 .
docker buildx build --push --tag bibica/caddy-supervisord-alpine --platform=linux/arm64,linux/amd64 .
````
### Mariadb v10.11.8 with Supervisord
```
docker buildx build --tag bibica/mariadb-supervisord-alpine -o type=image --platform=linux/arm64,linux/amd64 .
docker buildx build --push --tag bibica/mariadb-supervisord-alpine --platform=linux/arm64,linux/amd64 .
```
### PHP v8.3.10 with Supervisord
```
docker buildx build --tag bibica/php-supervisord-alpine -o type=image --platform=linux/arm64,linux/amd64 .
docker buildx build --push --tag bibica/php-supervisord-alpine --platform=linux/arm64,linux/amd64 .
```
Link images sau khi tạo xong
```
bibica/php-supervisord-alpine
bibica/mariadb-supervisord-alpine
bibica/caddy-supervisord-alpine
```
Mục đích tạo thêm Supervisord để tự khởi động lại dịch vụ nếu chẳng may có lỗi thôi, không có gì đặc biệt :D
