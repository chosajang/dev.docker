FROM php:7.4-fpm

RUN apt-get update && apt-get install -y \
    apt-utils \ 
    libfreetype6-dev \
    libjpeg-dev \
    libjpeg62-turbo-dev \
    libpng++-dev \ 
    libwebp-dev \ 
    libfreetype6-dev \ 
    libvpx-dev \ 
    libxpm-dev \ 
    libmcrypt-dev \
    libpng-dev \
    libssl-dev \
    libcurl4-openssl-dev \
    libpq-dev \
    libmemcached-dev \
    libzip-dev \
    libbz2-dev

RUN docker-php-ext-install bz2
RUN docker-php-ext-install curl
RUN docker-php-ext-install fileinfo
RUN docker-php-ext-install gettext
RUN docker-php-ext-install mbstring
RUN docker-php-ext-install mysqli

# GD
RUN docker-php-ext-configure gd --with-freetype --with-jpeg \
    && docker-php-ext-install -j "$(nproc)" gd

# RUN docker-php-ext-configure gd --with-freetype --with-jpeg \
#     && docker-php-ext-install -j$(nproc) gd \
#     && docker-php-ext-install mysqli
    # && docker-php-ext-install mbstring \ 
    # && docker-php-ext-install pdo \
    # && docker-php-ext-install pdo_mysql \ 
    # && docker-php-ext-install opcache

# os에서 필요한 유틸 설치
# RUN apt-get update -y && apt-get install -y apt-utils libzip-dev
# RUN git install
# RUN curl install
# RUN wget install
# RUN openssl
# RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer
# RUN docker-php-ext-install zip \
#     && docker-php-ext-install unzip

# RUN libpq-dev libmemcached-dev libzip-dev
# RUN libpng-dev libpng++-dev libjpeg-dev libjpeg62-turbo-dev libwebp-dev libfreetype6-dev libvpx-dev libxpm-dev libmcrypt-dev
# RUN libssl-dev libcurl4-openssl-dev
# RUN libmagick++-dev libmagickwand-dev libmagic-dev file

# # install GD
# RUN docker-php-ext-install iconv sockets mbstring mysqli pdo pdo_mysql \
#     && docker-php-ext-configure gd --with-freetype-dir=/usr/include/ --with-jpeg-dir=/usr/include/ \
#     && docker-php-ext-install gd \
#     && docker-php-ext-install intl \
#     && docker-php-ext-install zip

# RUN docker-php-ext-install mysqli && docker-php-ext-enable mysqli

# RUN apt-get install --yes --no-install-recommends apt-utils 
# RUN apt-get install --yes --no-install-recommends apt-transport-https

# RUN docker-php-ext-install curl fileinfo exif gettext
# RUN docker-php-ext-install json
# RUN docker-php-ext-install soap
# RUN docker-php-ext-install opcache
# RUN docker-php-ext-install phar

# # Install Memcached for php 7
# # RUN curl -L -o /tmp/memcached.tar.gz "https://github.com/php-memcached-dev/php-memcached/archive/php7.tar.gz" \
# #     && mkdir -p /usr/src/php/ext/memcached \
# #     && tar -C /usr/src/php/ext/memcached -zxvf /tmp/memcached.tar.gz --strip 1 \
# #     && docker-php-ext-configure memcached \
# #     && docker-php-ext-install memcached \
# #     && rm /tmp/memcached.tar.gz

# # Install memcached
# RUN set -ex \
#     && apt-get update \
#     && DEBIAN_FRONTEND=noninteractive apt-get install -y libmemcached-dev \
#     && rm -rf /var/lib/apt/lists/* \
#     && MEMCACHED="`mktemp -d`" \
#     && curl -skL https://github.com/php-memcached-dev/php-memcached/archive/master.tar.gz | tar zxf - --strip-components 1 -C $MEMCACHED \
#     && docker-php-ext-configure $MEMCACHED \
#     && docker-php-ext-install $MEMCACHED \
#     && rm -rf $MEMCACHED

# # Configure PHP
# RUN echo "\
# max_execution_time = 1200\n\
# max_input_time = -1\n\
# memory_limit = 2048M\n\
# upload_max_filesize = 2048M\n\
# post_max_size = 2048M\n\
# max_file_uploads = 20\n\
# default_charset = \"UTF-8\"\n\
# date.timezone = \"Asia/Seoul\"\n\
# short_open_tag = On" > /usr/local/etc/php/php.ini

# RUN pecl install xdebug-2.7.0beta1     && docker-php-ext-enable xdebug
# # Configure xDebug
# RUN echo "\
# xdebug.enable=1\n\
# xdebug.remote_enable=1\n\
# xdebug.remote_connect_back=0\n\
# xdebug.remote_port=9000\n\
# xdebug.remote_host=\"192.168.99.1\"\n\
# xdebug.idekey=\"PHPSTORM\"\n\
# xdebug.extended_info=on\n\
# xdebug.max_nesting_level=400\n\
# xdebug.var_display_max_depth=10\n\
# ">> /usr/local/etc/php/conf.d/docker-php-ext-xdebug.ini

# # Composer
# RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/bin --filename=composer
# RUN chmod +x /usr/bin/composer

# RUN usermod -u 1000 www-data
# RUN usermod -a -G users www-data

# # App dir
# RUN mkdir -p /var/www
# WORKDIR /var/www

# CMD [php-fpm]
# EXPOSE 9000