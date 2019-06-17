FROM golang:1.12-alpine3.9

ENV GOPATH /workspace
ENV PATH $GOPATH/bin:/usr/local/go/bin:$PATH

RUN apk update && \
    apk add --no-cache --update alpine-sdk git && \
    go get -u github.com/golang/dep/cmd/dep && \
    mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"

WORKDIR $GOPATH
