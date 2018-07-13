FROM php:alpine

LABEL maintainer="ahkui <ahkui@outlook.com>"

ARG PUID=1000
ENV PUID ${PUID}
ARG PGID=1000
ENV PGID ${PGID}
ARG DOCUMENT_ROOT=/var/www
ENV DOCUMENT_ROOT ${DOCUMENT_ROOT}/

RUN apk add --no-cache git

RUN cd /root && git clone https://github.com/mattpass/ICEcoder.git

RUN sed -i "s/\$_SERVER['DOCUMENT_ROOT']/getenv('DOCUMENT_ROOT',\$_SERVER['DOCUMENT_ROOT'])/g" /root/ICEcoder/lib/config___settings.php

WORKDIR /root/ICEcoder

CMD ["php","-S","0.0.0.0:80"]
