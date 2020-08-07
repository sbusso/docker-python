FROM sbusso/docker-python:base

LABEL maintainer="Stephane Busso <stephane.busso@gmail.com>"

RUN apk add --no-cache --virtual .build-deps build-base linux-headers python3-dev && \
  pip install --no-cache-dir "nltk==3.5" && \
  apk del .build-deps gcc libc-dev


RUN python -m nltk.downloader punkt