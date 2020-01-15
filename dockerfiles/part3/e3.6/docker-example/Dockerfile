#After
FROM python:3-alpine 

WORKDIR /usr/src/app

COPY . .
RUN pip install --no-cache -r requirements.txt &&\
    adduser -D app &&\
    chown -R app .

USER app

CMD python start.py