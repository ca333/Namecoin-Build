FROM ubuntu:bionic
MAINTAINER Komodo Platform support@komodoplatform.com

RUN apt-get update && \
    apt-get -y install \
    build-essential \
    pkg-config \
    libc6-dev \
    m4 \
    autoconf \
    curl \
    libtool \
    make \
    ncurses-dev \
    unzip \
    python \
    zlib1g-dev \
    wget \
    bsdmainutils \
    automake \
    libssl-dev \
    libprotobuf-dev \
    libevent-dev \
    protobuf-compiler \
    libqrencode-dev \
    libboost-all-dev \
    libcurl4-gnutls-dev \
    software-properties-common \
    libgconf-2-4 && \
    add-apt-repository ppa:bitcoin/bitcoin && \
    apt-get update && \
    apt-get install -y libdb4.8-dev libdb4.8++-dev && \
    apt-get -y clean; \
    rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

VOLUME /build
WORKDIR /build
