FROM python:3.8-alpine3.12

LABEL maintainer="Stephane Busso <stephane.busso@gmail.com>"

COPY requirements.txt ./requirements.txt

RUN apk add --no-cache --virtual .build-deps build-base linux-headers python3-dev && \
  pip install --no-cache-dir -r requirements.txt && \
  apk del .build-deps gcc libc-dev

RUN rm requirements.txt