FROM ubuntu:12.04
MAINTAINER Masahji Stewart <masahji@synctree.com>

ENV DEBIAN_FRONTEND noninteractive
RUN apt-get update -q && \
  apt-get install -qy \
  curl \
  less \
  screen \
  sudo \
  vim \
  telnet \
  git-core

RUN \
  adduser --disabled-password --gecos '' deploy && \
  echo 'deploy ALL=(ALL) NOPASSWD: ALL' > /etc/sudoers.d/deploy-sudo && \
  chmod 0400 /etc/sudoers.d/deploy-sudo

VOLUME /var/log
