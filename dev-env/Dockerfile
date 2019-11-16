FROM base-env:latest

USER root

RUN dnf install -y nodejs &&\
	npm i -g typescript &&\
	npm i -g sass

RUN dnf install -y java-1.8.0-openjdk-devel &&\
    dnf install -y maven

#RUN curl -s "https://get.sdkman.io" | bash
#RUN source "/root/.sdkman/bin/sdkman-init.sh"
#RUN sdk install gradle 6.0
#RUN sdk install kotlin

#RUN dnf install -y haskell-platform

USER dev-user

RUN curl https://sh.rustup.rs -sSf | sh -s -- -y
ENV PATH="/home/dev-user/.cargo/bin:${PATH}"
