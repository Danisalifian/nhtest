FROM php:7.2-apache

RUN apt-get update && apt-get install -y

RUN a2enmod rewrite
RUN docker-php-ext-install mysqli pdo_mysql

COPY boxbilling/www/  /var/www/html/

COPY --chown=www-data:www-data boxbilling/www/  /var/www/html/

RUN chown -R www-data:www-data /var/www/html/bb-data/cache
