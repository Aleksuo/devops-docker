FROM alpine:latest



RUN apk add --no-cache\
    python3 \
    libxml2 \
    ffmpeg \
    libxslt &&\
    apk add --no-cache --virtual .build-deps\
    py3-pip \
    python3-dev \
    build-base\
    libxml2-dev\
    libxslt-dev\
    && pip3 install --no-cache-dir --user --upgrade yle-dl \
    && apk del .build-deps\

WORKDIR /app

ENTRYPOINT ["/root/.local/bin/yle-dl"]

