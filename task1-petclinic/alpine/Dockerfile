FROM alpine:latest
RUN apk add --update --no-cache openssh openjdk11 git
RUN echo 'PasswordAuthentication yes' >> /etc/ssh/sshd_config
RUN adduser -h /home/mipi -s /bin/sh -D mipi
RUN echo -n 'mipi:pimi' | chpasswd
COPY entrypoint.sh /
ENTRYPOINT ["/entrypoint.sh"]

#ENTRYPOINT [ "tail", "-f", "/dev/null" ]