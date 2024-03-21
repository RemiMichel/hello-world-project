FROM php:8.3-fpm

COPY --from=composer/composer:latest-bin /composer /usr/bin/composer

RUN apt-get update && \
    apt-get upgrade -y && \
    apt-get install -y git unzip

COPY . /var/www/html/

WORKDIR /var/www/html

ENTRYPOINT ["/var/www/html/entrypoint.sh"]

CMD ["php-fpm"]