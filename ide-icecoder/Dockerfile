FROM zuohuadong/caddy:alpine

LABEL maintainer="ahkui <ahkui@outlook.com>"

RUN cd /root && git clone https://github.com/mattpass/ICEcoder.git

WORKDIR /root/ICEcoder

RUN echo -e '0.0.0.0:80 {\n    root /root/ICEcoder\n    fastcgi / php-fpm:9000 php {\n        index index.php\n    }\n}' >> /root/Caddyfile

CMD ["/usr/bin/caddy", "-agree","-conf","/root/Caddyfile"]
