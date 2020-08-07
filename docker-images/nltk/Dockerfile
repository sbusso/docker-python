FROM sbusso/docker-python:base

LABEL maintainer="Stephane Busso <stephane.busso@gmail.com>"

COPY requirements.txt ./requirements.txt

RUN pip install --no-cache-dir -r requirements.txt

RUN rm requirements.txt