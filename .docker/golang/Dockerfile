FROM golang:1.14-alpine

ENV GO111MODULE on

RUN mkdir /go/src/app

COPY ./api /go/src/app

WORKDIR /go/src/app

RUN apk add --no-cache git \
  && go build -o app \
  && go get github.com/oxequa/realize

CMD ["./app"]
