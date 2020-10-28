FROM node:12.18.1-alpine3.9


WORKDIR /env

COPY wait-for-it.sh /env/wait-for-it.sh

RUN apk update && apk upgrade && apk add bash && apk add git && apk add curl && mkdir /root/.font && apk add zsh && apk add wget && \
    wget --directory-prefix=/root/.font https://github.com/romkatv/powerlevel10k-media/raw/master/MesloLGS%20NF%20Regular.ttf && \
    wget --directory-prefix=/root/.font https://github.com/romkatv/powerlevel10k-media/raw/master/MesloLGS%20NF%20Bold.ttf && \
    wget --directory-prefix=/root/.font https://github.com/romkatv/powerlevel10k-media/raw/master/MesloLGS%20NF%20Italic.ttf && \
    wget --directory-prefix=/root/.font https://github.com/romkatv/powerlevel10k-media/raw/master/MesloLGS%20NF%20Bold%20Italic.ttf && \
    wget https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh && \
    sh install.sh && rm install.sh && \
    git clone https://github.com/zsh-users/zsh-completions ${ZSH_CUSTOM:=/root/.oh-my-zsh/custom}/plugins/zsh-completions && \
    git clone --depth=1 https://github.com/romkatv/powerlevel10k.git /root/powerlevel10k && \
    echo 'source /root/powerlevel10k/powerlevel10k.zsh-theme' >> /root/.zshrc && \
    touch  /tmp/out && mkdir /code
