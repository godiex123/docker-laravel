FROM composer:latest

WORKDIR /var/www/html

# Definir el home de Composer para evitar que use /tmp
ENV COMPOSER_HOME=/var/www/.composer
ENV PATH="$COMPOSER_HOME/vendor/bin:$PATH"

# Copiar configuración de PHP si es necesario
COPY --from=php /usr/local/etc/php /usr/local/etc/php

# Forzar la creación de la carpeta de Composer y asegurar permisos correctos
RUN mkdir -p $COMPOSER_HOME \
    && chown -R www-data:www-data $COMPOSER_HOME \
    && composer global config bin-dir --absolute

# Instalar el instalador de Laravel de manera global
RUN composer global require laravel/installer

CMD ["composer"]

