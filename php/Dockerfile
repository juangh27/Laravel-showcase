# Use an official PHP Apache image
FROM php:8.2-apache

# Update package lists and install dependencies
RUN apt-get update \
    && apt-get install -y \
        g++ \
        libicu-dev \
        libzip-dev \
        zip \
        zlib1g-dev \
        libpq-dev \
    && rm -rf /var/lib/apt/lists/*

# Install PHP extensions
RUN docker-php-ext-install \
    intl \
    opcache \
    pdo \
    pdo_mysql

# Set the working directory
WORKDIR /var/www/laravel_docker

# Install Composer globally
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

# Set the correct permissions for the working directory
RUN chown -R www-data:www-data /var/www/laravel_docker

# Apache configuration: enable mod_rewrite
RUN a2enmod rewrite

# Restart Apache to apply changes
RUN service apache2 restart
