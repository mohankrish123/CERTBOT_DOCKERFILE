# CERTBOT_DOCKERFILE

FROM nginx:latest

LABEL maintainer="Mohan Krishna V<mohankrishnav@kensium.com>"

RUN apt-get update \   
    && apt-get -y install nginx nano vim net-tools curl wget \   
    && export LANG=en_US.UTF-8 \   
    && apt-get update \   
    && apt-get install -y software-properties-common    
RUN apt-get update   
RUN add-apt-repository ppa:certbot/certbot   
RUN apt-get install certbot python3 python python-certbot-nginx python3-certbot-nginx -y   
### certbot --email mohankrish3@gmail.com --agree-tos --no-eff-email -d certbot.mohank.tk   
