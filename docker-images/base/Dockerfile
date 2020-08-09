FROM python:3.8-slim

LABEL maintainer="Stephane Busso <stephane.busso@gmail.com>"

RUN apt-get update && apt install -y --no-install-recommends git && \
  apt autoremove && apt clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* 

COPY requirements.txt ./requirements.txt

RUN pip install --no-cache-dir -r requirements.txt

RUN rm requirements.txt

ENV PYTHONUNBUFFERED True
ENV APP_HOME=/app
ENV WORKERS=1 
WORKDIR $APP_HOME

CMD exec gunicorn --bind :$PORT --workers $WORKERS --threads 8 --timeout 0 app:app