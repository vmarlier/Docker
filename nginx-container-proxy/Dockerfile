FROM ubuntu:14.04

MAINTAINER Eranga Bandara (erangaeb@gmail.com)

# install nginx
RUN apt-get update -y
RUN apt-get install -y python-software-properties
RUN apt-get install -y software-properties-common
RUN add-apt-repository -y ppa:nginx/stable
RUN apt-get update -y
RUN apt-get install -y nginx
RUN rm /etc/nginx/sites-available/*
RUN rm /etc/nginx/sites-enabled/*

# deamon mode off
RUN echo "\ndaemon off;" >> /etc/nginx/nginx.conf
RUN chown -R www-data:www-data /var/lib/nginx

# volume
VOLUME ["/etc/nginx/sites-enabled", "/etc/nginx/certs", "/var/log/nginx"]

# expose ports
EXPOSE 80 443

# add nginx conf
ADD bookstack.conf /etc/nginx/conf.d/default.conf

WORKDIR /etc/nginx

CMD ["nginx"]

