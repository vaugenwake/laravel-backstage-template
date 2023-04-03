FROM php:8.2-fpm-alpine3.17 as base

ENV PHP_VERSION=php

RUN \
    cd /tmp \
    && apk add --no-cache \
    libmcrypt-dev \
    zlib-dev \
    jq

COPY . /var/www/html

CMD ["php-fpm", "-F"]

FROM base AS consumer
CMD ["php", "/var/www/html/artisan", "queue:consume"]
