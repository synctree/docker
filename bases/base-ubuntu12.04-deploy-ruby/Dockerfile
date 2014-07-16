FROM synctree/base-ubuntu12.04-deploy

RUN \
  echo "install: --no-rdoc --no-ri" > /home/deploy/.gemrc && \
  chown deploy:deploy /home/deploy/.gemrc

RUN su - deploy -c 'curl -L https://get.rvm.io | bash -s stable --ruby=2.1.2 --gems=bundler'
