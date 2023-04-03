FROM nginx:stable-alpine

COPY .docker/nginx/config/nginx.conf /etc/nginx/nginx.conf
COPY .docker/nginx/config/default.conf.template /etc/nginx/templates/default.conf.template

COPY ./public /var/www/html/public
