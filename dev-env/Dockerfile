FROM base-env:latest

USER root

RUN dnf install -y nodejs &&\
#	npm i -g tern &&\
	npm i -g typescript &&\
	npm i -g sass

#RUN dnf install -y haskell-platform

USER dev-user

RUN curl https://sh.rustup.rs -sSf | sh -s -- -y
ENV PATH="/home/dev-user/.cargo/bin:${PATH}"
