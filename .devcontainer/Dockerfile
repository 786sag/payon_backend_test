FROM mcr.microsoft.com/devcontainers/php:8.2

RUN apt-get update && apt-get install -y \
    unzip zip git curl nano \
    libpng-dev libonig-dev libxml2-dev \
    default-mysql-client redis-tools supervisor

RUN curl -fsSL https://deb.nodesource.com/setup_lts.x | bash \
    && apt-get install -y nodejs

RUN composer self-update
