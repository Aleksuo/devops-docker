FROM node:13-alpine

WORKDIR /app

RUN apk add --no-cache --virtual .dep \
    git &&\
    git clone https://github.com/docker-hy/frontend-example-docker.git . && \
    npm install &&\
    apk del .dep

CMD API_URL=http://localhost:8000 npm start