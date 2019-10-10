FROM base-env:latest

USER root

RUN dnf install -y nodejs &&\
    npm i -g typescript &&\
	npm i -g sass

RUN dnf install -y haskell-platform

USER dev-user

RUN curl https://sh.rustup.rs -sSf | sh -s -- -y
ENV PATH="/home/dev-user/.cargo/bin:${PATH}"
#    dnf install -y java-1.8.0-openjdk-devel &&\
#    dnf install -y maven &&\
#    dnf install -y gradle &&\
