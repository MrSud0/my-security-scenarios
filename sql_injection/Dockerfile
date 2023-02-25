FROM php:7.2-apache

# Update packages and install dependencies
RUN apt-get update && \
    apt-get install -y git && \
    rm -rf /var/lib/apt/lists/*

# Clone vulnerable web application and set up Apache
RUN git clone https://github.com/bobbytables/SQLInjectionSampleApp.git /var/www/html
RUN echo "ServerName localhost" >> /etc/apache2/apache2.conf

# Expose port 80
EXPOSE 80

CMD ["apache2-foreground"]
