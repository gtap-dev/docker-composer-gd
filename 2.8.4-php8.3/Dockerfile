FROM php:8.3-alpine

ENV COMPOSER_ALLOW_SUPERUSER=1
ENV COMPOSER_HOME=/tmp

RUN apk add --no-cache libpng-dev libzip-dev zlib-dev

# The official composer image also installs the zip extension
RUN docker-php-ext-install gd zip

RUN curl --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer
RUN php /tmp/installer.php --install-dir=/usr/bin --filename composer --version=2.8.4

CMD ["composer"]
