FROM node:13-alpine as build-stage

WORKDIR /app

RUN apk add --no-cache --virtual .dep \
    git &&\
    git clone https://github.com/docker-hy/frontend-example-docker.git . && \
    npm install &&\
    apk del .dep &&\
    API_URL=http://localhost:8000 npm run build &&\
    adduser -D app &&\
    chown -R app .
    

USER app

FROM  node:13-alpine

WORKDIR /site

COPY --from=build-stage /app/dist /site
RUN npm install -g serve


CMD serve -s -l 5000 /site