FROM php:7.2-fpm

COPY php.ini /usr/local/etc/php

# install composer 
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer
# install php xdebug 
RUN pecl install xdebug
# create-user
RUN adduser dev
COPY test.php /home/dev
