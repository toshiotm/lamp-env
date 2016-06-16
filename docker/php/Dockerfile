FROM php:7.0-apache

RUN apt-get update
RUN apt-get install -y \ 
    libicu-dev \ 
    libpq-dev
RUN docker-php-ext-install intl
RUN docker-php-ext-install pdo_pgsql
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

RUN rm /etc/apache2/apache2.conf
COPY ./apache2.conf /etc/apache2/apache2.conf


RUN a2enmod rewrite

