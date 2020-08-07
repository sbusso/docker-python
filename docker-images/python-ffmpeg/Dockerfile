FROM mwader/static-ffmpeg AS ffmpeg

FROM sbusso/docker-python:base

COPY --from=ffmpeg /ffmpeg /usr/local/bin/

# ENV LIBRARY_PATH=/lib:/usr/lib

RUN pip install --no-cache-dir "moviepy==1.0.3"
