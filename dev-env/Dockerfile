FROM base-env:latest

USER root

RUN dnf install -y java-1.8.0-openjdk-devel &&\
	dnf install -y maven &&\
	dnf install -y gradle &&\
        dnf install -y nodejs &&\
	dnf install -y nodejs-yarn &&\
	npm install -g @angular/cli

USER david
