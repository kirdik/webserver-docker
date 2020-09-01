FROM php:5.6.29-fpm
RUN apt-get update && apt-get install -y \
            curl \
            wget \
            libfreetype6-dev \
            libjpeg62-turbo-dev \
            libmcrypt-dev \
            libxml2-dev \
            && docker-php-ext-install mysql gd mcrypt zip
ADD php.ini /usr/local/etc/php/conf.d/40-custom.ini
WORKDIR /var/www
CMD ["php-fpm"]
