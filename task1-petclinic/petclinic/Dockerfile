FROM maven:alpine as build
RUN apk add git
RUN git clone https://github.com/spring-projects/spring-petclinic.git
COPY application-mysql.properties /spring-petclinic/src/main/resources
WORKDIR /spring-petclinic
RUN mvn clean install

FROM alpine:latest
ENV spring_profiles_active mysql
RUN apk update\
    apk upgrade
RUN apk add --no-cache openjdk11
RUN mkdir -p /home/spring-petclinic
COPY --from=build /spring-petclinic/target/spring-petclinic-2.7.3.jar /home/spring-petclinic
WORKDIR /home/spring-petclinic
ENTRYPOINT java -jar spring-petclinic-2.7.3.jar

