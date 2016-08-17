FROM alpine:3.4

ENV GOPATH /repo:/repo/Godeps/_workspace

RUN apk update && \
    apk add git go && \
    git clone https://github.com/samsung-cnct/setup-network-environment.git /repo && \
    cd /repo && \
    go build && \
    mv repo /networking-setup && \
    cd / && \
    rm -rf /repo && \
    apk del git go

CMD /networking-setup
