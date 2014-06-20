FROM synctree/bases:ubuntu-12.04-deploy-stable

RUN su - deploy -c "rvm install ruby-2.0.0-p353"
RUN su - deploy -c "rvm gemset create logg"

RUN su - deploy -c "mkdir -p /home/deploy/app/logg"
