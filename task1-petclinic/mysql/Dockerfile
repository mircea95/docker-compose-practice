FROM alpine:latest

WORKDIR /app

RUN apk add --update mysql mysql-client && rm -f /var/cache/apk/*

COPY start.sh /startup.sh
RUN dos2unix /startup.sh
ENTRYPOINT ["/startup.sh"]
