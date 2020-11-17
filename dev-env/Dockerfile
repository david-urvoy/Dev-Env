FROM davidurvoy/base-env:latest

RUN mkdir -p /home/dev-user/.cargo
#VOLUME [ "/home/dev-user/.cargo" ]

USER root
RUN dnf install -y nodejs
RUN dnf install -y make automake gcc gcc-c++ kernel-devel

USER dev-user
### NPM ###
ENV NPM_CONFIG_PREFIX="/home/dev-user/.npm-global"
RUN npm i -g yarn typescript tslint sass
#RUN npm i -g expo-cli

### RUST ###
RUN curl https://sh.rustup.rs -sSf | sh -s -- -y
ENV PATH="/home/dev-user/.cargo/bin:${PATH}"

