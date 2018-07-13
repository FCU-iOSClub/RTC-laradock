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

RUN php -r '$str=file_get_contents("/root/ICEcoder/lib/settings-system-params.php");print($str);$str=str_replace("docRoot", "docRoot\"=> getenv(\"DOCUMENT_ROOT\",\"/var/www/\"), //",$str);file_put_contents("/root/ICEcoder/lib/settings-system-params.php", $str);'

WORKDIR /root/ICEcoder

CMD ["php","-S","0.0.0.0:80"]
