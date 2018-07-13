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

WORKDIR /root/ICEcoder

CMD ["php","-S","0.0.0.0:80"]
