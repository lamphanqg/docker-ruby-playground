FROM ubuntu:18.04
ENV LANG C.UTF-8
ENV TZ Asia/Tokyo

RUN apt-get update
RUN apt-get install -y curl vim git-core build-essential libssl-dev libreadline-dev zlib1g-dev postgresql-client libpq-dev tzdata
RUN curl -sL https://deb.nodesource.com/setup_12.x | bash -
RUN curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | apt-key add -
RUN echo "deb https://dl.yarnpkg.com/debian/ stable main" | tee /etc/apt/sources.list.d/yarn.list
RUN apt-get update
RUN apt-get install -y nodejs yarn

RUN export PATH="$HOME/.rbenv/bin:$HOME/.rbenv/shims:$PATH"
RUN curl -fsSL https://github.com/cykerway/rbenv-installer/raw/master/bin/rbenv-installer | bash
RUN echo 'export PATH="$HOME/.rbenv/bin:$HOME/.rbenv/shims:$PATH"' >> $HOME/.bashrc
RUN echo 'eval "$(rbenv init -)"' >> $HOME/.bashrc

RUN mkdir /projects