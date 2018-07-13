FROM php:alpine

LABEL maintainer="ahkui <ahkui@outlook.com>"

RUN apk add --no-cache git

RUN cd /var/www && git clone https://github.com/mattpass/ICEcoder.git

WORKDIR /var/www/ICEcoder

CMD ["php","-S","0.0.0.0:80"]
