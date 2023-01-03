FROM alpine:3.16.2

RUN apk update\
    apk upgrade
RUN apk add --no-cache openjdk11 jenkins

VOLUME [ "/jenkis_data" ]
WORKDIR "/usr/share/webapps/jenkins/"
ENTRYPOINT ["java", "-jar","jenkins.war"]