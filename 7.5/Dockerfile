FROM php:7.5-fpm
RUN apt-get update && apt-get install -y \
        libfreetype6-dev \
        libjpeg62-turbo-dev \
        libpng-dev \
        librabbitmq-dev \
        libxml2-dev \
        libmcrypt-dev \
        libonig-dev \
    && docker-php-ext-install -j$(nproc) gd \
    && docker-php-ext-install -j$(nproc) pdo \
    && docker-php-ext-install -j$(nproc) pdo_mysql \
    && docker-php-ext-install -j$(nproc) xml \
    && docker-php-ext-install -j$(nproc) mbstring \
    && pecl install redis \
    && pecl install swoole \
    && pecl install amqp \
    && pecl install mcrypt \
    && docker-php-ext-enable redis swoole amqp mcrypt

