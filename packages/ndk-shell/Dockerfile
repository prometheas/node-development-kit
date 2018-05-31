FROM alpine

RUN apk --update add -U \
  curl \
  bash \
  ca-certificates \
  openssl \
  ncurses \
  coreutils \
  python2 \
  make \
  gcc \
  g++ \
  libgcc \
  linux-headers \
  grep \
  util-linux \
  binutils \
  findutils

RUN touch /root/.profile \
  && echo 'export NVM_DIR="$HOME/.nvm"' >> /root/.profile \
  && echo '[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"' >> /root/.profile \
  && echo '[ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion"' >> /root/.profile

RUN curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.11/install.sh | bash \
  && bash -l -c 'nvm install --lts'

RUN apk add \
  git \
  less \
  zsh
