FROM php:7.2-apache

# Update packages and install dependencies
RUN apt-get update && \
    apt-get install -y git && \
    rm -rf /var/lib/apt/lists/*

# Set up Apache web server
RUN echo "ServerName localhost" >> /etc/apache2/apache2.conf
COPY index.php /var/www/html/
COPY style.css /var/www/html/
COPY script.js /var/www/html/
COPY contact.php /var/www/html/
COPY success.php /var/www/html/
COPY error.php /var/www/html/
COPY README.md /var/www/html/
COPY FLAG.txt /flag.txt
RUN chown -R www-data:www-data /var/www/html/ && \
    chmod -R 755 /var/www/html/

# Add Easter egg image and hide clue using steganography
COPY easter-egg.jpg /var/www/html
RUN echo "Can you find the hidden clue in the image? Use steganography to extract it." >> /var/www/html/easter-egg.jpg

# Expose port 80
EXPOSE 80

CMD ["apache2-foreground"]
