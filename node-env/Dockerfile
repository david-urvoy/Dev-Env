FROM base-env:latest

USER root

RUN dnf install -y nodejs &&\
    npm i -g tern &&\
    npm i -g typescript &&\
    npm i -g sass

USER dev-user

RUN nvim +PlugInstall +qall
