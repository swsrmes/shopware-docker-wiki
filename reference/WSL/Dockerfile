FROM ghcr.io/shyim/shopware-docker/6/nginx:php74-xdebug

RUN apk add bash nano busybox-extras
RUN mv /usr/local/etc/php/conf.d/xdebug.ini /usr/local/etc/php/conf.d/xdebug.ini.default
COPY xdebug.ini /usr/local/etc/php/conf.d/xdebug.ini
