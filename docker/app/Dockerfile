FROM php:7.0.10-fpm-alpine

RUN apk update && apk add -U git libmemcached zlib

RUN docker-php-source extract \
    && git clone --branch php7 https://github.com/php-memcached-dev/php-memcached /usr/src/php/ext/memcached/ \
    && docker-php-ext-install memcached zip \
    && docker-php-source delete