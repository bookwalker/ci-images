FROM ubuntu:bionic

RUN apt-get -y update \ 
    && apt-get -y install git-core \
    && apt-get -y install ruby \
    && apt-get remove --purge --auto-remove -y ca-certificates \
    && rm -rf /var/lib/apt/lists/* 
