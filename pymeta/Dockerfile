FROM python:3.7.3-alpine3.9

RUN apk add --no-cache shadow bash git && \
    git clone --depth 1 https://github.com/m8r0wn/pymeta && \
    mkdir -p /pymeta/output && \
    useradd --create-home --shell /sbin/nologin pymeta

WORKDIR /pymeta/

RUN chown -R pymeta:pymeta /pymeta && \
    python3 setup.py install

USER pymeta

ENTRYPOINT ["python3", "/pymeta/pymeta.py"]