FROM jrottenberg/ffmpeg:4.3-alpine as ffmpeg

FROM sbusso/docker-python:base


COPY --from=ffmpeg /usr/local /usr/local

WORKDIR /
COPY requirements.txt ./

RUN apk add --no-cache --virtual .build-deps gcc g++ build-base linux-headers \
  ca-certificates python3-dev libffi-dev libressl-dev && \
  ln -s /usr/include/local.h /usr/include/xlocale.h && \
  pip install --no-cache-dir "moviepy==1.0.3" && \
  apk --purge del .build-deps
RUN rm requirements.txt