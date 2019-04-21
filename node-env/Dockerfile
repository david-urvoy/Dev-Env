FROM dev-env:latest

USER root

RUN dnf install -y nodejs &&\
	dnf install -y nodejs-yarn &&\
	npm i -g sass

USER david
