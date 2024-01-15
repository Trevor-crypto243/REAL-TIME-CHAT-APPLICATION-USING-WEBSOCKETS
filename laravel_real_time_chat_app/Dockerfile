FROM php:8.2-fpm

WORKDIR /var/www/html

RUN apt-get update && \
    apt-get install -y \
        libzip-dev \
        zip \
        unzip

RUN docker-php-ext-install pdo pdo_mysql zip

# Install Composer globally
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

RUN composer require beyondcode/laravel-websockets

# Copy the Laravel project files, including the artisan file
COPY --chown=www-data:www-data . /var/www/html

CMD ["php", "artisan", "serve", "--host=0.0.0.0", "--port=8000"]

