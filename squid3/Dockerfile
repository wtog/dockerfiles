FROM ubuntu:14.04

ADD apt/sources.list /etc/apt/

RUN apt-get -qy update && apt-get -qy install vim \
                                              wget \
                                              curl \
                                              tar \
                                              squid3 \
                                              apache2-utils \
                                              && rm -rf /var/lib/apt/lists/*
COPY squid.conf /etc/squid3/squid.conf
RUN htpasswd -bc /etc/squid3/passwd demo demo
# ENTRYPOINT ["/bin/bash"]
ENTRYPOINT ["squid3", "-N"]