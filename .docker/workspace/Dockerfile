FROM ubuntu:18.04

FROM composer:2.0

FROM php:8.0

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

RUN curl -sL https://deb.nodesource.com/setup_14.x | bash

RUN apt-get install -y nodejs

COPY --from=composer:2.0 /usr/bin/composer /usr/bin/composer

WORKDIR /var/www/html