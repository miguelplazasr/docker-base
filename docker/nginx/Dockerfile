FROM alpine:3.7

MAINTAINER MiguelPlazasR <miguelplazasr@gmail.com>

RUN apk add --update nginx
RUN rm -rf /var/cache/apk/* && rm -rf /tmp/*

ADD nginx.conf /etc/nginx/
ADD symfony.conf /etc/nginx/conf.d/
ADD laravel.conf /etc/nginx/laravel.conf
ADD crux.conf /etc/nginx/conf.d/
ADD cors_support /etc/nginx/cors_support

RUN echo "upstream php-upstream { server php:9001; }" > /etc/nginx/conf.d/upstream.conf

RUN adduser -D -g '' -G www-data www-data

#COPY --from=build-stage /var/www/crux/dist/out/ /usr/share/nginx/html

CMD ["nginx"]

EXPOSE 80
EXPOSE 8080
EXPOSE 443
