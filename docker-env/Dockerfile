FROM php:8.2-apache

WORKDIR /var/www/html

RUN docker-php-ext-install mysqli  pdo pdo_mysql
RUN a2enmod rewrite

# Permitir .htaccess y mod_rewrite
RUN sed -i 's/AllowOverride None/AllowOverride All/g' /etc/apache2/apache2.conf

EXPOSE 80

RUN chown -R www-data:www-data /var/www/html \
    && chmod -R 755 /var/www/html