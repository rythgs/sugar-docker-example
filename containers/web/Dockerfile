FROM php:8.3-apache

RUN usermod -u 1000 www-data && groupmod -g 1000 www-data

RUN  apt-get -qqy update \
  && apt-get -y install vim \
  && apt-get -y install libpng-dev libjpeg-dev \
  && apt-get -y install re2c libmcrypt-dev \
  && apt-get -y install zlib1g-dev \
  && apt-get -y install libssl-dev libc-client2007e-dev libkrb5-dev \
  && apt-get -y install libcurl4-gnutls-dev \
  && apt-get -y install libxml2-dev libxslt-dev \
  && apt-get -y install libssl-dev \
  && apt-get -y install libcurl4-openssl-dev \
  && apt-get -y install libzip-dev \
  && apt-get -y install libonig-dev

RUN  docker-php-ext-install bcmath \
  && docker-php-ext-configure gd --with-jpeg=/usr/lib \
  && docker-php-ext-install gd \
  && docker-php-ext-configure imap --with-imap-ssl --with-kerberos \
  && docker-php-ext-install imap \
  && docker-php-ext-install mysqli \
  && docker-php-ext-install pdo_mysql \
  && docker-php-ext-install zip \
  && docker-php-ext-install soap \
  && docker-php-ext-install opcache

COPY config/crm.php.ini /usr/local/etc/php/conf.d/

RUN a2enmod headers expires deflate rewrite

EXPOSE 80

VOLUME ["/var/www"]
