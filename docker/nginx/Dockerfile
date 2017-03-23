FROM ubuntu:latest

RUN apt-get update \
    && apt-get install -y nginx \
    && chown -R www-data:www-data /var/lib/nginx

# EXPOSE 80 443

CMD ["nginx", "-g", "daemon off;"]