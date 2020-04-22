FROM frolvlad/alpine-glibc:alpine-3.10_glibc-2.29
LABEL securibee (@securibee)

RUN apk add --no-cache wget && \
  wget -O /usr/bin/findomain https://github.com/Edu4rdSHL/findomain/releases/latest/download/findomain-linux && \
  chmod +x /usr/bin/findomain

ENTRYPOINT ["/usr/bin/findomain"]