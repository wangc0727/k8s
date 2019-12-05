FROM php:7.1-fpm
RUN apt-get update && apt-get install -y \
        libfreetype6-dev \
        libjpeg62-turbo-dev \
        libpng-dev \
    && docker-php-ext-install -j$(nproc) iconv \
    && docker-php-ext-configure gd --with-freetype-dir=/usr/include/ --with-jpeg-dir=/usr/include/ \
       --with-gettext \
       --with-kerberos \
       --with-pcre-regex \
       --with-pdo-sqlite \
       --with-libdir=lib64 \
       --with-openssl \
       --with-xsl \
       --with-xmlrpc \
       --with-mysqli \
       --with-pear \
       --with-libxml-dir \
       --with-png-dir \
       --with-freetype-dir \
       --with-iconv-dir \
       --with-zlib \
       --with-curl \
       --enable-soap \
       --enable-ftp \
       --enable-mbstring \
       --enable-sockets \
       --enable-exif \
       --enable-fpm \
       --enable-bcmath \
       --enable-inline-optimization \
       --enable-mbregex \
       --enable-opcache \
       --enable-pcntl \
       --enable-shmop \
       --enable-sysvsem \
       --enable-xml \
       --enable-zip \
       --with-xpm-dir \
       --with-pdo-mysql \
    && docker-php-ext-install -j$(nproc) gdv
