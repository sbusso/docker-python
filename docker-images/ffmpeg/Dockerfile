FROM debian:buster-slim

RUN apt-get update && apt install -y --no-install-recommends ffmpeg && \
  apt autoremove && apt clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* 