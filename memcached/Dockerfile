FROM alpine:latest

RUN \
  apk --update add memcached wget && \
  wget --no-check-certificate -O /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/1.7/gosu-amd64 && \
  chmod +x /usr/local/bin/gosu && \
  mkdir /data && chown memcached:memcached /data && \
  rm -rf /var/cache/apk/*

VOLUME /data
WORKDIR /data

EXPOSE 11211

ENTRYPOINT ["gosu", "memcached", "memcached"]
