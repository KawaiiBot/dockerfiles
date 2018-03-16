FROM python:alpine
MAINTAINER aurieh <me@aurieh.me>

ENV LIBRARY_PATH=/lib:/usr/lib

RUN apk update && apk upgrade && \
    apk add build-base python-dev py-pip jpeg-dev zlib-dev freetype-dev
