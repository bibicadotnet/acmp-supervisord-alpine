# Dockerfile ACMP Supervisord Alpine

### Caddy 2.8.4 with Supervisord
```
docker buildx create --name mybuilder
docker buildx use mybuilder
docker buildx build --tag bibica/caddy-supervisord-alpine -o type=image --platform=linux/arm64,linux/amd64 .
docker buildx build --push --tag bibica/caddy-supervisord-alpine --platform=linux/arm64,linux/amd64 .
````
### Mariadb v10.11.8 with Supervisord
```
docker buildx build --tag bibica/mariadb-supervisord-alpine -o type=image --platform=linux/arm64,linux/amd64 .
docker buildx build --push --tag bibica/mariadb-supervisord-alpine --platform=linux/arm64,linux/amd64 .
```
### Mariadb v10.11.8 with Supervisord
```
docker buildx build --tag bibica/php-supervisord-alpine -o type=image --platform=linux/arm64,linux/amd64 .
docker buildx build --push --tag bibica/php-supervisord-alpine --platform=linux/arm64,linux/amd64 .
```















