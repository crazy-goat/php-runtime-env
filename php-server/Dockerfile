FROM alpine

COPY www /var/www

RUN apk update \
    && apk add php composer \
    && cd /var/www \
    && composer install -o --no-dev

ENTRYPOINT php -S 0.0.0.0:80 -t /var/www