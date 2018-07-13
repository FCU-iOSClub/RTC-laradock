FROM zuohuadong/caddy:alpine

LABEL maintainer="ahkui <ahkui@outlook.com>"

RUN cd /root && git clone https://github.com/mattpass/ICEcoder.git

WORKDIR /root/ICEcoder

CMD ["/usr/bin/caddy", "-agree","-host","0.0.0.0"]
