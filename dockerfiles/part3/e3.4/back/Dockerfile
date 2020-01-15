FROM node:13-alpine

WORKDIR /app

RUN apk add --no-cache --virtual .dep \
    git &&\
    git clone https://github.com/docker-hy/backend-example-docker.git . && \
    npm install &&\
    apk del .dep &&\
    adduser -D app &&\
    chown -R app .

USER app

CMD FRONT_URL=http://localhost:5000 npm start