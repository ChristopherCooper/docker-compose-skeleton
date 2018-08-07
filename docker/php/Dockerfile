FROM php:7.2-fpm

WORKDIR /var/www

RUN apt-get update; apt-get install -y \
        libcurl4-gnutls-dev \
        libsqlite3-0 \
        libxml2-dev \
        libz-dev \
        libicu-dev \
        curl \
        mysql-client \
        cron

## PHP Extensions
RUN docker-php-ext-install curl
RUN docker-php-ext-install json
RUN docker-php-ext-install mbstring
RUN docker-php-ext-install pdo
RUN docker-php-ext-install pdo_mysql
RUN docker-php-ext-install xml
RUN docker-php-ext-install zip

COPY ./crontab /etc/cron.d/crons

RUN chmod 0644 /etc/cron.d/crons
RUN crontab /etc/cron.d/crons

COPY ./entrypoint.sh /
RUN chmod 0777 /entrypoint.sh
ENTRYPOINT /entrypoint.sh