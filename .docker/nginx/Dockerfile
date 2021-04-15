FROM nginx:1.19-alpine

LABEL maintainer="DucLS <ducls.coder@gmail.com>"

ADD ./.docker/nginx/conf.d/default.conf /etc/nginx/conf.d/default.conf
ADD ./.docker/nginx/nginx.conf /etc/nginx/nginx.conf

RUN mkdir -p /var/www/html

RUN addgroup -g 1000 laravel

RUN adduser -D -u 1000 laravel -G laravel

RUN chown -R laravel:laravel /var/www/html