FROM alpine:3.7

LABEL maintainer="MiguelPlazasR <miguelplazasr@gmail.com>"

RUN apk add --update \
    php7-fpm \
    php7-apcu \
    php7-ctype \
    php7-curl \
    php7-dom \
    php7-gd \
    php7-iconv \
    php7-imagick \
    php7-json \
    php7-intl \
    php7-mcrypt \
    php7-mbstring \
    php7-opcache \
    php7-openssl \
    php7-pdo \
    php7-pdo_mysql \
    php7-mysqli \
    php7-xml \
    php7-xmlwriter \
    php7-zlib \
    php7-phar \
    php7-tokenizer \
    php7-session \
    php7-simplexml \
    make \
    curl

RUN apk update && apk add ca-certificates && update-ca-certificates && apk add openssl

RUN rm -rf /var/cache/apk/* && rm -rf /tmp/*

RUN curl --insecure https://getcomposer.org/composer.phar -o /usr/bin/composer && chmod +x /usr/bin/composer

RUN composer config --global repo.packagist composer https://packagist.org

RUN composer self-update

ADD backend.ini /etc/php7/php-fpm.d/
ADD backend.ini /etc/php7/cli/conf.d/

ADD backend.pool.conf /etc/php7/php-fpm.d/

CMD ["php-fpm7", "-F"]

WORKDIR /var/www/backend
EXPOSE 9000
