FROM ubuntu:18.04

# Update packages and install dependencies
RUN apt-get update && \
    apt-get install -y openssl && \
    rm -rf /var/lib/apt/lists/*

# Copy vulnerable web server configuration
COPY server.conf /etc/apache2/sites-available/000-default.conf

# Set up Apache web server
RUN a2enmod ssl && \
    a2ensite default-ssl && \
    echo "ServerName localhost" >> /etc/apache2/apache2.conf && \
    sed -i '/<IfModule mod_ssl.c>/a SSLProtocol all -SSLv3 -TLSv1 -TLSv1.1' /etc/apache2/mods-available/ssl.conf

# Expose ports 80 and 443
EXPOSE 80
EXPOSE 443

CMD ["apache2ctl", "-D", "FOREGROUND"]