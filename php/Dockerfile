FROM php:8.3-fpm

RUN set -eux; \
    apt-get update; \
    apt-get install -y --no-install-recommends \
        libpng-dev libjpeg-dev libfreetype6-dev libicu-dev libzip-dev \
        libonig-dev libxml2-dev zip unzip curl; \
    docker-php-ext-configure gd --with-freetype --with-jpeg; \
    docker-php-ext-install -j$(nproc) gd intl zip mysqli opcache; \
    rm -rf /var/lib/apt/lists/*

RUN { \
      echo "upload_max_filesize=64M"; \
      echo "post_max_size=64M"; \
      echo "memory_limit=256M"; \
      echo "max_execution_time=120"; \
    } > /usr/local/etc/php/conf.d/wp.ini

WORKDIR /var/www/html
