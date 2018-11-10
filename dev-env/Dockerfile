FROM fedora:latest

RUN dnf install -y zsh &&\
	dnf install -y git &&\
	sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)" &&\
	mkdir -p /home/david/emacs &&\
	git clone https://github.com/syl20bnr/spacemacs /home/david/emacs/.emacs.d &&\
	mkdir -p /home/david/config &&\
	--mount=target=/home/david/config,type=bind,source=/home/david/config

ENTRYPOINT /bin/zsh
