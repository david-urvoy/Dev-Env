FROM david-urvoy/base-env:latest

USER root
RUN dnf install -y nodejs

USER dev-user
### NPM ###
ENV NPM_CONFIG_PREFIX="/home/dev-user/.npm-global"
RUN npm i -g yarn typescript sass
#RUN npm i -g expo-cli

