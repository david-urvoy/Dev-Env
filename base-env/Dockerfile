FROM fedora:latest

RUN     dnf install -y zsh &&\
	dnf install -y curl &&\
#	dnf install -y ping &&\
	dnf install -y neovim &&\
	dnf install -y tmux &&\
	dnf install -y git

RUN sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"

RUN dnf install -y powerline-fonts

RUN useradd -u 1001 -d /home/david -ms /bin/bash david
USER david
WORKDIR /home/david

ENTRYPOINT /bin/zsh
