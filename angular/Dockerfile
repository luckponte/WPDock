FROM ubuntu:latest

# INSTALL SYSTEM DEPENDENCIES
RUN apt-get update && apt-get install curl python git make build-essential -y

# INSTALL NODEJS
RUN curl -sL https://deb.nodesource.com/setup_8.x | bash -
RUN apt-get install nodejs -y
RUN chmod -R 777 /usr/
RUN npm install -g bower
RUN useradd -c 'Node.js user' -m -d /home/node -s /bin/bash node
USER node

RUN npm install -g typescript
RUN npm install -g @angular/cli@latest
RUN npm install -g gulp

USER root
RUN NVM_NODEJS_ORG_MIRROR="" 
