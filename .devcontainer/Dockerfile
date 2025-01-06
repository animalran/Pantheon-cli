# Use Ubuntu 20.04 as the base image
FROM ubuntu:20.04

# Set noninteractive mode for apt
ENV DEBIAN_FRONTEND=noninteractive

# Install required packages
RUN apt-get update && apt-get install -y \
    php7.4-cli \
    php7.4-xml \
    php7.4-mbstring \
    php7.4-curl \
    php7.4-zip \
    git \
    openssh-client \
    composer \
    curl \
    unzip && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

# Add Composer to PATH
ENV PATH="$PATH:/root/.composer/vendor/bin"
