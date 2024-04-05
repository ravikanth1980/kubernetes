FROM php:8.1-apache

# Install MySQL driver for PHP
RUN docker-php-ext-install mysqli && docker-php-ext-enable mysqli

#RUN a2enmod php

# Copy Apache configuration file to enable mod_rewrite
COPY apache2.conf /etc/apache2/apache2.conf

# Enable mod_rewrite
RUN a2enmod rewrite

# Copy your PHP application files into the container
#COPY . /var/www/html/
