# Dockerfile ACMP Supervisord Alpine
Sử dụng Docker Desktop để tạo
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















