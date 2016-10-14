FROM node:latest

RUN apt -qq update \
 && apt -qq upgrade -y \
 && apt -qq install -y ocaml libelf-dev ruby-dev rubygems \
 && apt -qq install -y pinentry-curses libarchive13 libgpgme11 gnupg2 libassuan0 gnupg-agent libksba8 libpth20 \
 && wget -O /tmp/reprepo_amd64.deb http://ftp.debian.org/debian/pool/main/r/reprepro/reprepro_4.17.1-1~bpo8+1_amd64.deb \
 && dpkg -i /tmp/reprepo_amd64.deb \
 && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* \
 && gem install fpm