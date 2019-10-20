FROM octava/php7.2-cli


# create-user
RUN adduser dev

COPY php.ini /usr/local/etc/php

COPY composer.json /home/dev
COPY test.php /home/dev

COPY launch.json /.vscode/

WORKDIR /home/dev
# install composer 
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer && \
    composer install

# enable xdebug 
RUN docker-php-ext-enable xdebug

