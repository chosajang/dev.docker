FROM httpd:2.4

# Common Install
RUN apt-get update
RUN apt-get install -y software-properties-common
RUN apt-get update

# Apache Install
RUN apt-get install -y php7.3 php7.3-common php7.3-cli
RUN apt-get install php7.3-bcmath php7.3-bz2 php7.3-curl php7.3-gd php7.3-intl php7.3-json php7.3-mbstring php7.3-readline php7.3-xml php7.3-zip -y
RUN apt-get install libapache2-mod-php7.3