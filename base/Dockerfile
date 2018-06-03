FROM debian:jessie

ENV TERM=linux

RUN apt-get update \
    && apt-get install -y --no-install-recommends git curl ca-certificates nano \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* /usr/share/doc/*
