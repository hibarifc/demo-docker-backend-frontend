FROM php:7.4.9-apache-buster
RUN apt-get update \
    && apt-get install -y libzip-dev \
    && apt-get install -y zlib1g-dev \
    && apt-get install -y libicu-dev \
    && rm -rf /var/lib/apt/lists/* \
    && docker-php-ext-install zip \
    && docker-php-ext-install pdo_mysql intl

COPY config/apache.conf /etc/apache2/sites-available/000-default.conf