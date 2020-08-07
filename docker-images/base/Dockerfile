FROM python:3.8-slim

LABEL maintainer="Stephane Busso <stephane.busso@gmail.com>"

COPY requirements.txt ./requirements.txt

RUN pip install --no-cache-dir -r requirements.txt

RUN rm requirements.txt