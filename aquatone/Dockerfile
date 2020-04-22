FROM alpine:latest

ENV VERSION=1.7.0

# Installs latest Chromium package.
RUN echo @edge http://nl.alpinelinux.org/alpine/edge/community > /etc/apk/repositories \
    && echo @edge http://nl.alpinelinux.org/alpine/edge/main >> /etc/apk/repositories \
    && apk add --no-cache \
    libstdc++@edge \
    chromium@edge \
    harfbuzz@edge \
    nss@edge \
    freetype@edge \
    ttf-freefont@edge \
    && rm -rf /var/cache/* \
    && mkdir /var/cache/apk

# install aquatone binary
WORKDIR /opt/aquatone
RUN wget https://github.com/michenriksen/aquatone/releases/download/v${VERSION}/aquatone_linux_amd64_${VERSION}.zip && \
    unzip aquatone_linux_amd64_${VERSION}.zip && \
    cp aquatone /

ENTRYPOINT ["/aquatone"]