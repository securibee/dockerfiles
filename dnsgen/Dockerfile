FROM alpine:3.11
LABEL securibee (@securibee)

# This hack is widely applied to avoid python printing issues in docker containers.
# See: https://github.com/Docker-Hub-frolvlad/docker-alpine-python3/pull/13
ENV PYTHONUNBUFFERED=1

RUN echo "**** install Python and Git ****" && \
    apk add --no-cache python3 git && \
    if [ ! -e /usr/bin/python ]; then ln -sf python3 /usr/bin/python ; fi && \
    \
    echo "**** install pip ****" && \
    python3 -m ensurepip && \
    rm -r /usr/lib/python*/ensurepip && \
    pip3 install --no-cache --upgrade pip setuptools wheel && \
    if [ ! -e /usr/bin/pip ]; then ln -s pip3 /usr/bin/pip ; fi && \
    echo "**** install dnsgen ****" && \
    git clone https://github.com/ProjectAnte/dnsgen && \
    cd dnsgen && \
    pip3 install -r requirements.txt && \
    python3 setup.py install