FROM base-env:latest


RUN dnf install -y nodejs &&\
    npm i -g typescript &&\
	npm i -g sass

RUN dnf install -y go

RUN dnf install -y rust

RUN dnf install -y ghc cabal-install

#    dnf install -y java-1.8.0-openjdk-devel &&\
#    dnf install -y maven &&\
#    dnf install -y gradle &&\
#	dnf install -y nodejs-yarn &&\
#	npm install -g @angular/cli &&\
