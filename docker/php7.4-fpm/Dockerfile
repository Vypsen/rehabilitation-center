FROM php:7.4-fpm

RUN apt-get update && apt-get install -y \
    git \
    zip \
    libpq-dev \
    wget \
    zlib1g-dev \
    libmcrypt-dev \
    libzip-dev \
    openssl

RUN docker-php-ext-install pdo pdo_pgsql zip
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer
RUN curl -sS https://get.symfony.com/cli/installer

WORKDIR /var/www/project

CMD ["php-fpm"]

