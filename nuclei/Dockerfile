FROM golang:alpine
LABEL maintainer="th3_alchem1st"

RUN apk add --no-cache git

RUN mkdir -p /tools
WORKDIR /tools

RUN GO111MODULE=on go get -v github.com/projectdiscovery/nuclei/v2/cmd/nuclei
RUN mv /go/bin/nuclei /tools/nuclei

RUN git clone https://github.com/projectdiscovery/nuclei-templates.git

ENTRYPOINT ["/tools/nuclei"]
