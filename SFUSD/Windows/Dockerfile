FROM ubuntu:bionic
MAINTAINER Komodo Platform support@komodoplatform.com

RUN apt-get update && apt-get -y install \
  autoconf \
  automake \
  autogen \
  bsdmainutils \
  build-essential \
  cmake \
  curl \
  libc6-dev \
  libcap-dev \
  libcurl4-gnutls-dev \
  libqrencode-dev \
  libprotobuf-dev \
  libssl-dev \
  libtool \
  libz-dev \
  libbz2-dev \
  m4 \
  make \
  g++-mingw-w64-x86-64 \
  ncurses-dev \
  pkg-config \
  protobuf-compiler \
  python \
  python-zmq \
  software-properties-common \
  unzip \
  wget \
  zip \
  zlib1g-dev && \
  add-apt-repository ppa:bitcoin/bitcoin && \
  apt-get update && \
  apt-get install -y libdb4.8-dev libdb4.8++-dev && \
  update-alternatives --install /usr/bin/x86_64-w64-mingw32-g++ x86_64-w64-mingw32-g++ /usr/bin/x86_64-w64-mingw32-g++-win32 60 && \
  update-alternatives --install /usr/bin/x86_64-w64-mingw32-g++ x86_64-w64-mingw32-g++ /usr/bin/x86_64-w64-mingw32-g++-posix 90 && \
  update-alternatives --config x86_64-w64-mingw32-g++ && \
  apt-get -y autoremove; \
  apt-get -y autoclean; \
  apt-get -y clean && \
  rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

VOLUME /build
WORKDIR /build
