FROM dev-env:latest

USER root

RUN dnf install -y java-1.8.0-openjdk-devel &&\
	dnf install -y maven &&\
	dnf install -y gradle &&\
	mkdir -p /home/david/development/projects/java

USER david
