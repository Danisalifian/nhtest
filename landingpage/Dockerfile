FROM php:7.2-apache

RUN apt-get update && apt-get install -y

RUN a2enmod rewrite
RUN docker-php-ext-install mysqli pdo_mysql

COPY .  /var/www/html/