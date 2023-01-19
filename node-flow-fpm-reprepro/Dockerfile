FROM node:16-bullseye

RUN curl -sS http://dl.yarnpkg.com/debian/pubkey.gpg | apt-key add - \
 && echo "deb http://dl.yarnpkg.com/debian/ stable main" | tee /etc/apt/sources.list.d/yarn.list \
 && apt -qq update \
 && apt -qq install -y apt-utils \
 && apt -qq upgrade -y \
 && apt -qq install -y ocaml libelf-dev ruby-dev rubygems python3 pinentry-curses libarchive13 libgpgme11 gnupg2 libassuan0 gnupg-agent libksba8 libjpeg-dev libpng-dev libwebp-dev libtiff-dev libpth20 yarn \
 && update-alternatives --install /usr/bin/python python3 /usr/bin/python3.9 10 \
 && wget -O /tmp/reprepo_amd64.deb http://ftp.debian.org/debian/pool/main/r/reprepro/reprepro_5.3.0-1_amd64.deb \
 && dpkg -i /tmp/reprepo_amd64.deb \
 && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* \
 && gem install fpm
