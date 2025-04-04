FROM php:fpm-alpine

# Instalar extensiones necesarias para Laravel
RUN apk add --no-cache \
    bash \
    zip \
    unzip \
    curl \
    libpng-dev \
    oniguruma-dev \
    freetype-dev \
    libjpeg-turbo-dev \
    icu-dev \
    && docker-php-ext-configure gd --with-freetype --with-jpeg \
    && docker-php-ext-install gd pdo pdo_mysql mbstring opcache intl

# Copiar configuración personalizada
COPY php.ini /usr/local/etc/php/php.ini

# Establecer directorio de trabajo
WORKDIR /var/www/html

