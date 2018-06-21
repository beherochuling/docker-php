FROM phpdockerio/php72-cli

RUN export DEBIAN_FRONTEND=noninteractive \
    && apt-get update \
    && apt-get -y --no-install-recommends install php7.2-fpm php7.2-mysql php7.2-gd \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* /usr/share/doc/*

COPY overrides.conf /etc/php/7.2/fpm/pool.d/z-overrides.conf

COPY php-fpm-startup /usr/bin/php-fpm
CMD /usr/bin/php-fpm

EXPOSE 9000
