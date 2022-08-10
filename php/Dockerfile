FROM php:fpm-alpine

WORKDIR /srv/www

ADD https://github.com/mlocati/docker-php-extension-installer/releases/latest/download/install-php-extensions /usr/local/bin/

RUN chmod +x /usr/local/bin/install-php-extensions \
    && install-php-extensions @composer-2.0.2 \
    && install-php-extensions bcmath pdo_mysql mysqli ldap 

