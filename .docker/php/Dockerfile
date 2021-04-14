FROM php:8.0-fpm-alpine

LABEL maintainer="DucLs <ducls.coder@gmail.com>"

ADD ./.docker/php/www.conf /usr/local/etc/php-fpm.d/www.conf

RUN mkdir -p /var/www/html

RUN addgroup -g 1001 laravel

RUN adduser -D -u 1001 laravel -G laravel

RUN chown -R laravel:laravel /var/www/html

RUN docker-php-ext-install \
  bcmath \
  pdo_mysql

USER laravel
