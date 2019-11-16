FROM base-env:latest

USER root

RUN dnf install -y nodejs

RUN dnf install -y java-1.8.0-openjdk-devel &&\
    dnf install -y maven

#RUN curl -s "https://get.sdkman.io" | bash
#RUN source "/root/.sdkman/bin/sdkman-init.sh"
#RUN sdk install gradle 6.0
#RUN sdk install kotlin

#RUN dnf install -y haskell-platform

USER dev-user

ENV NPM_CONFIG_PREFIX="/home/dev-user/.npm-global"

RUN npm i -g typescript sass

RUN npm i -g expo-cli

RUN curl https://sh.rustup.rs -sSf | sh -s -- -y
ENV PATH="/home/dev-user/.cargo/bin:${PATH}"
