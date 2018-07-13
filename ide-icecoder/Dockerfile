FROM php:alpine

LABEL maintainer="ahkui <ahkui@outlook.com>"

RUN apk add --no-cache git

RUN cd /root && git clone https://github.com/mattpass/ICEcoder.git

WORKDIR /root/ICEcoder

CMD ["php","-S","0.0.0.0:80"]
