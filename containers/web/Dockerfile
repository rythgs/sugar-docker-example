FROM php:8.4-apache

RUN usermod -u 1000 www-data && groupmod -g 1000 www-data

ADD --chmod=0755 https://github.com/mlocati/docker-php-extension-installer/releases/latest/download/install-php-extensions /usr/local/bin/

RUN apt-get -qqy update \
  && apt-get -y install vim \
  && apt-get clean \
  && rm -rf /var/lib/apt/lists/*

RUN install-php-extensions \
    bcmath \
    gd \
    imap \
    mysqli \
    pdo_mysql \
    zip \
    soap \
    opcache

COPY config/crm.php.ini /usr/local/etc/php/conf.d/

RUN a2enmod headers expires deflate rewrite

EXPOSE 80

VOLUME ["/var/www"]
