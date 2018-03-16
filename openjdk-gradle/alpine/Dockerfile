FROM openjdk:alpine
MAINTAINER aurieh <me@aurieh.me>
ENV GRADLE_VERSION "4.6"

RUN apk update && apk upgrade && apk add curl

RUN curl -Os --location https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip && \
  mkdir /opt && \
  unzip -q gradle-${GRADLE_VERSION}-bin.zip -d /opt && \
  ln -s /opt/gradle-${GRADLE_VERSION} /opt/gradle && \
  rm -f gradle-${GRADLE_VERSION}-bin.zip

ENV PATH=${PATH}:/opt/gradle/bin
