FROM fedora:latest

RUN     dnf install -y zsh &&\
	dnf install -y curl &&\
#	dnf install -y ping &&\
	dnf install -y neovim &&\
	dnf install -y tmux &&\
	dnf install -y git
RUN dnf install -y powerline-fonts

RUN useradd -u 1001 -d /home/dev-user -ms /bin/bash dev-user
USER dev-user
WORKDIR /home/dev-user

RUN sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
RUN curl -fLo ~/.local/share/nvim/site/autoload/plug.vim --create-dirs https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim

RUN mkdir -p /home/dev-user/development/projects
RUN git clone https://github.com/DavidUrvoy/Bash-Config.git /home/dev-user/development/config
RUN . /home/dev-user/development/config/install.sh

ENTRYPOINT /bin/zsh
