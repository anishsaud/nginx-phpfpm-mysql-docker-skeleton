FROM php:fpm-alpine

WORKDIR /srv/www

RUN docker-php-ext-install -j$(nproc) bcmath pdo_mysql \
    && docker-php-ext-enable pdo_mysql bcmath

RUN apk add --no-cache --virtual .build-deps $PHPIZE_DEPS \
    && pecl install xdebug \
    && docker-php-ext-enable xdebug \
    && apk del -f .build-deps

COPY --from=composer:latest /usr/bin/composer /usr/local/bin/composer

# RUN mv "$PHP_INI_DIR/php.ini-development" "$PHP_INI_DIR/php.ini"
# RUN mv "$PHP_INI_DIR/php.ini-production" "$PHP_INI_DIR/php.ini"

