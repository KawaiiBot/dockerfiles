FROM golang:alpine
MAINTAINER aurieh <me@aurieh.me>

ENV GLIDE_VER v0.13.1
RUN RUN \
	apk add -q --no-cache --virtual .build-deps git && \
	go get github.com/Masterminds/glide                 && \
	cd ${GOPATH}/src/github.com/Masterminds/glide       && \
	TAG=$(git tag | grep ${GLIDE_VER} | sort | tail -1) && \
	git checkout -q ${TAG}                                 && \
	go install
