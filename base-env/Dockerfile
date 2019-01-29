FROM fedora:latest

RUN useradd -ms /bin/bash david &&\
	dnf install -y zsh &&\
	dnf install -y tmux &&\
	dnf install -y git &&\
	sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)" &&\
	dnf install -y powerline-fonts &&\
	dnf install -y emacs &&\
	dnf install -y vim &&\
	mkdir -p /home/david/development/config

USER david
WORKDIR /home/david

ENTRYPOINT /bin/zsh
