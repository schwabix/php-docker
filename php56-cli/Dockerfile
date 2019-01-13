FROM php:5.6-cli-alpine

MAINTAINER michael@schwabix.de

# Install PECL extensions
RUN apk add --no-cache --virtual .build-deps autoconf build-base \
  && docker-php-ext-install mysqli \
  && pecl install xdebug-2.5.0 \
  && docker-php-ext-enable xdebug \
  && apk del .build-deps \
  && rm -rf /tmp/pear ~/.pearrc
