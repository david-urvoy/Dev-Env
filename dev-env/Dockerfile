FROM fedora:latest

WORKDIR /app

COPY . /app

RUN dnf install -y zsh &&\
	dnf install -y tmux &&\
	dnf install -y git &&\
	sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)" &&\
	dnf install -y powerline-fonts &&\
	mkdir -p /home/david/development/projects &&\
	mkdir -p /home/david/development/config &&\
	mkdir -p /home/david/emacs &&\
	git clone https://github.com/syl20bnr/spacemacs /home/david/emacs/.emacs.d &&\
	cat bash-config >> /root/.bashrc &&\
	. /root/.bashrc &&\
	cp .zshrc $HOME/.zshrc

ENTRYPOINT /bin/zsh
