FROM golang:alpine AS build
LABEL maintainer="th3_alchem1st"

RUN apk add --no-cache git

RUN go get -u github.com/tomnomnom/assetfinder
RUN go get -u github.com/tomnomnom/httprobe
RUN go get -u github.com/tomnomnom/meg
RUN go get -u github.com/tomnomnom/unfurl
RUN go get -u github.com/tomnomnom/waybackurls
RUN go get -u github.com/tomnomnom/anew

FROM alpine

COPY --from=build /go/bin/* /usr/local/bin/
RUN apk update \
 && apk add jq \
 && rm -rf /var/cache/apk/*

CMD "/bin/ash"
