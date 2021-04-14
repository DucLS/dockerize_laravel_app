FROM ubuntu:18.04

LABEL maintainer="DucLs <ducls.coder@gmail.com>"

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

RUN mkdir -p /var/www/html

RUN groupadd -g 1000 laravel

RUN useradd -u 1000 -g laravel -s /bin/sh laravel

RUN chown -R laravel:laravel /var/www/html

USER laravel