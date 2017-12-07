FROM php:7.1.12-fpm-jessie

RUN apt-get update && apt-get install -y \
        libfreetype6-dev \
        libjpeg62-turbo-dev \
        libmcrypt-dev \
        libmysql++-dev\
    	libpng12-dev \
    	libicu-dev \
    	libxslt1-dev \
        libedit-dev \
        librecode-dev \
        libxml++2.6-dev \
        libxml2-dev \
    && docker-php-ext-install -j$(nproc) iconv mcrypt soap readline recode zip xml intl xsl pdo_mysql \
    && docker-php-ext-configure gd --with-png-dir=/usr/include/ --with-freetype-dir=/usr/include/ --with-jpeg-dir=/usr/include/ \
    && docker-php-ext-install -j$(nproc) gd

COPY php.ini /usr/local/etc/php/