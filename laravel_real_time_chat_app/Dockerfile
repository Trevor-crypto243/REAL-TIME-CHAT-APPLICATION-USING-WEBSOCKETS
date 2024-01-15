FROM php:8.2-fpm

WORKDIR /var/www/html

RUN apt-get update && \
    apt-get install -y \
        libzip-dev \
        zip \
        unzip

RUN docker-php-ext-install pdo pdo_mysql zip

# Copy the Laravel project files, including the artisan file
COPY --chown=www-data:www-data . /var/www/html

CMD ["php", "artisan", "serve", "--host=0.0.0.0", "--port=8000"]

