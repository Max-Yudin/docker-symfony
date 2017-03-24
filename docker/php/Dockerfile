FROM ubuntu:latest

RUN apt-get update \
&&  apt-get -y install php7.0 \
    php7.0-cli \
    php7.0-curl \
    php7.0-gd \
    php7.0-json \
    php7.0-mysql \
    php7.0-xml \
    php7.0-fpm \
    php7.0-intl \
    php7.0-mbstring \
    php7.0-zip \
&& php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');" \
&& php -r "if (hash_file('SHA384', 'composer-setup.php') === '669656bab3166a7aff8a7506b8cb2d1c292f042046c5a994c43155c0be6190fa0355160742ab2e1c88d40d5be660b410') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;" \
&& php composer-setup.php --install-dir=bin --filename=composer

RUN mkdir -p /run/php/

CMD ["php-fpm7.0", "-F"]