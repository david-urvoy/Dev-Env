FROM fedora:latest

RUN dnf install -y zsh &&\
	dnf install -y tmux &&\
	dnf install -y git &&\
	sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)" &&\
	dnf install -y powerline-fonts &&\
	git clone https://github.com/syl20bnr/spacemacs ~/emacs/.emacs.d

ENTRYPOINT /bin/zsh
