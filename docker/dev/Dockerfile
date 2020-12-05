FROM php:8.0-cli

RUN apt update \
    && apt install git libzip-dev zip -y \
    && docker-php-ext-install zip

WORKDIR /app

COPY --from=composer:2.0.7 /usr/bin/composer /usr/bin/composer

CMD composer install && tail -f /dev/null
