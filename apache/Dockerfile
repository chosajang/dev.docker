FROM httpd:2.4

# Common Install
RUN apt-get update && apt-get install -y \
    apt-utils \
    git \
    wget \
    libtool \
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
    libbz2-dev \
    libxml2-dev

# Apache Install
RUN apt-get install -y php7.3 php7.3-common php7.3-cli
RUN apt-get install -y php7.3-bcmath php7.3-bz2 php7.3-curl php7.3-gd php7.3-intl php7.3-json php7.3-mbstring php7.3-readline php7.3-xml php7.3-zip
RUN apt-get install -y libapache2-mod-php7.3