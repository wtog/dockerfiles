FROM wtog/openjdk8:latest

RUN echo http://mirrors.ustc.edu.cn/alpine/v3.8/main > /etc/apk/repositories && \
    echo http://mirrors.ustc.edu.cn/alpine/v3.8/community >> /etc/apk/repositories

RUN apk update && apk upgrade
ENV LANG C.UTF-8
ARG SBT_VERSION=1.3.2

RUN wget -c "https://piccolo.link/sbt-${SBT_VERSION}.tgz" && \
    tar -zxf sbt-${SBT_VERSION}.tgz -C /usr/local && \
    ln -s /usr/local/sbt/bin/sbt /usr/local/bin/sbt && \
    chmod 755 /usr/local/bin/sbt && \
    rm sbt-${SBT_VERSION}.tgz
