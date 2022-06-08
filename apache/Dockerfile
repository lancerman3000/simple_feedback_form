FROM php:7.4-apache
RUN apt-get update && apt-get install -y \
    curl \
    wget \
    libzip-dev \
    libxml2-dev \
    libmagickwand-dev --no-install-recommends \
    libssl-dev libcurl4-openssl-dev \
    && pecl install imagick \
    && docker-php-ext-install -j$(nproc) mysqli pdo_mysql zip curl \
    && docker-php-ext-install exif soap sockets \
    && docker-php-ext-enable imagick 
EXPOSE 80