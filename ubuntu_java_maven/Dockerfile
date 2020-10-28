FROM ubuntu:20.04

ARG DEBIAN_FRONTEND=noninteractive

RUN apt-get update && \
    apt-get install -y openjdk-11-jdk maven git zsh wget locales && \
    wget --directory-prefix=/usr/share/fonts/truetype https://github.com/romkatv/powerlevel10k-media/raw/master/MesloLGS%20NF%20Regular.ttf && \
    wget --directory-prefix=/usr/share/fonts/truetype https://github.com/romkatv/powerlevel10k-media/raw/master/MesloLGS%20NF%20Bold.ttf && \
    wget --directory-prefix=/usr/share/fonts/truetype https://github.com/romkatv/powerlevel10k-media/raw/master/MesloLGS%20NF%20Italic.ttf && \
    wget --directory-prefix=/usr/share/fonts/truetype https://github.com/romkatv/powerlevel10k-media/raw/master/MesloLGS%20NF%20Bold%20Italic.ttf && \
    wget https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh && sh install.sh && rm install.sh && \
    git clone https://github.com/zsh-users/zsh-completions ${ZSH_CUSTOM:=~/.oh-my-zsh/custom}/plugins/zsh-completions && \
    sed -i -e 's/# en_US.UTF-8 UTF-8/en_US.UTF-8 UTF-8/' /etc/locale.gen && \
    dpkg-reconfigure --frontend=noninteractive locales && \
    update-locale LANG=en_US.UTF-8 && \
    touch  /tmp/out && mkdir /code

ENTRYPOINT [ "tail", "-f", "/tmp/out" ]
