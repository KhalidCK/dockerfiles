FROM python:3-alpine

RUN apk add \
        --no-cache \
        curl \
        wget \
        tree \
        neovim \
        bc \
        g++ \
        git \
        groff \
        libgcc \
        libstdc++ \
        make \
        ncurses \
        ncurses-dev \
        sudo \
        fzf \
        fish \
        ansible \
        util-linux
RUN apk del \
            --no-cache \
            g++ \
            make \
            ncurses-dev
RUN fish -c true \
    && adduser \
        -D \
        -u 1000 \
        -s /usr/local/bin/fish \
        kh \
    && echo 'kh ALL=(ALL) NOPASSWD: ALL' >> /etc/sudoers

ENV SHELL /usr/bin/fish
RUN pip install --no-cache visidata httpie
USER kh
WORKDIR /home/kh
#fisher extra
RUN curl https://git.io/fisher --create-dirs -sLo ~/.config/fish/functions/fisher.fish
RUN fish -c "fisher add matchai/spacefish"
CMD ["fish"]