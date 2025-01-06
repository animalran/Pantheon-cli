# Use a PHP base image
FROM php:8.1-cli

# Install Composer and required tools
RUN apt-get update && apt-get install -y \
    curl \
    git \
    unzip \
    && curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

# Install Pantheon CLI using Composer
RUN composer create-project pantheon-systems/terminus /usr/local/bin/terminus --no-dev --prefer-dist

# Set up the terminal environment
ENV PATH="/usr/local/bin/terminus:${PATH}"
