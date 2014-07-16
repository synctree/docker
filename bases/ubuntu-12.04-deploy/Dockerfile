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
  chmod 0400 /etc/sudoers.d/deploy-sudo && \
  echo "install: --no-rdoc --no-ri" > /home/deploy/.gemrc && \
  chown deploy:deploy /home/deploy/.gemrc

RUN su - deploy -c 'curl -L https://get.rvm.io | bash -s stable --ruby=2.1.2 --gems=bundler'

VOLUME /var/log
