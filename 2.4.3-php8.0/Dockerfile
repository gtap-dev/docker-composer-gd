FROM php:8.0-alpine

ENV COMPOSER_ALLOW_SUPERUSER 1
ENV COMPOSER_HOME /tmp

RUN apk add --no-cache libpng-dev libzip-dev zlib-dev

# The official composer image also installs the zip extension
RUN docker-php-ext-install gd zip

RUN curl --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/0a51b6fe383f7f61cf1d250c742ec655aa044c94/web/installer
RUN php /tmp/installer.php --install-dir=/usr/bin --filename composer --version=2.4.3

CMD ["composer"]
