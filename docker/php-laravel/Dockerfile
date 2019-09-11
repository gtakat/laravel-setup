FROM php:7.3-fpm

ARG DIR="/webapp"

WORKDIR $DIR

ENV DEBIAN_FRONTEND noninteractive
ENV COMPOSER_ALLOW_SUPERUSER 1
ENV COMPOSER_NO_INTERACTION 1

RUN set -e \
      && apt-get update -y -qq \
      && apt-get install -y -qq git zip tzdata net-tools dnsutils procps \
      && cp /usr/share/zoneinfo/Asia/Tokyo /etc/localtime \
      && echo "Asia/Tokyo" > /etc/timezone

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

RUN composer global require hirak/prestissimo

