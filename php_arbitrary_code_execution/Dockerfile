FROM php:7.2-apache

# Update packages and install dependencies
RUN apt-get update && \
    apt-get install -y git && \
    rm -rf /var/lib/apt/lists/*

# Clone vulnerable PHP script and add hidden clues
RUN git clone https://github.com/vulhub/phpggc.git /var/www/html/phpggc && \
    echo "You're getting closer. The next clue is hidden in the source code." >> /var/www/html/phpggc/gadgetchains/monolog/RCE.php && \
    echo "The next clue is hidden in an image. Can you find it?" >> /var/www/html/phpggc/gadgetchains/symfony/RCE4.php

# Set up Apache web server and add Easter eggs
RUN echo "ServerName localhost" >> /etc/apache2/apache2.conf
COPY index.php /var/www/html
COPY image.jpg /var/www/html  # This is an Easter egg!

# Expose port 80
EXPOSE 80

CMD ["apache2-foreground"]
