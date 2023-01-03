FROM alpine:latest
RUN apk update &&\
    apk upgrade
RUN apk add nginx
COPY default.conf /etc/nginx/http.d/default.conf
ENTRYPOINT ["nginx", "-g", "daemon off;"]