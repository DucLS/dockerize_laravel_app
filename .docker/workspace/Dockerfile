FROM composer:2.0

FROM php:8.0

LABEL maintainer="DucLs <ducls.coder@gmail.com>"

COPY --from=composer:2.0 /usr/bin/composer /usr/bin/composer

RUN apt-get update && apt-get install -y \
  software-properties-common locales

RUN apt-get update && apt-get install -y \
  git \
  curl \
  vim \
  nano \
  net-tools \
  pkg-config \
  iputils-ping

RUN docker-php-ext-install \
  bcmath \
  pdo_mysql

RUN curl -sL https://deb.nodesource.com/setup_14.x | bash

RUN apt-get install -y nodejs

RUN mkdir -p /var/www/html

RUN groupadd -g 1000 laravel

RUN useradd -u 1000 -g laravel -s /bin/sh laravel

RUN chown -R laravel:laravel /var/www/html

COPY ./src /var/www/html

USER laravel