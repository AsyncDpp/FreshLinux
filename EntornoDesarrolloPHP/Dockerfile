# Dockerfile
FROM php:8.3-apache

# Habilitar mod_rewrite
RUN a2enmod rewrite

# Copiar configuración personalizada de Apache (opcional)
COPY apache.conf /etc/apache2/sites-available/000-default.conf
