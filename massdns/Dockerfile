FROM alpine:latest
LABEL securibee (@securibee)

RUN apk --no-cache add --virtual native-deps \
    g++ gcc libgcc libstdc++ linux-headers git make && \
    git clone --depth 1 https://github.com/blechschmidt/massdns.git

WORKDIR /massdns/
RUN make

ENTRYPOINT ["./bin/massdns"]

