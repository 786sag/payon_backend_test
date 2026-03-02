FROM mcr.microsoft.com/devcontainers/php:8.2

# Install system tools
RUN apt-get update && apt-get install -y \
    unzip zip git curl nano \
    libpng-dev libonig-dev libxml2-dev \
    default-mysql-server redis-server \
    supervisor

# Enable MySQL to run inside Codespaces
RUN sed -i 's/bind-address/#bind-address/' /etc/mysql/mysql.conf.d/mysqld.cnf

# Install Node.js LTS
RUN curl -fsSL https://deb.nodesource.com/setup_lts.x | bash \
    && apt-get install -y nodejs

# Update composer
RUN composer self-update
