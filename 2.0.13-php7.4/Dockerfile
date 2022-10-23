FROM php:7.4-alpine

ENV COMPOSER_ALLOW_SUPERUSER 1
ENV COMPOSER_HOME /tmp

RUN apk add --no-cache libpng-dev libzip-dev zlib-dev

# The official composer image also installs the zip extension
RUN docker-php-ext-install gd zip

RUN curl --output /tmp/installer.php --url https://raw.githubusercontent.com/composer/getcomposer.org/9b15acb8cb2cdaf2207f2bff8c0412ede0e7bd5b/web/installer
RUN php /tmp/installer.php --install-dir=/usr/bin --filename composer --version=2.0.13

CMD ["composer"]
