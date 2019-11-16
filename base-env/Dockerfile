FROM fedora:latest

RUN dnf install -y zsh curl neovim tmux nodejs git unzip zip which
RUN dnf install -y powerline-fonts

RUN dnf install -y python
RUN pip3 install pynvim

RUN useradd -u 1001 -d /home/dev-user -ms /bin/bash dev-user
USER dev-user
WORKDIR /home/dev-user

RUN sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"

# neovim
RUN curl -fLo ~/.local/share/nvim/site/autoload/plug.vim --create-dirs https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim

# config folder & install configuration
RUN mkdir -p /home/dev-user/development/projects
RUN git clone https://github.com/DavidUrvoy/Bash-Config.git /home/dev-user/development/config
RUN . /home/dev-user/development/config/install.sh

RUN nvim +PlugInstall +qall

ENTRYPOINT /bin/zsh
