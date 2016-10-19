FROM node:0.12

RUN apt -qq update \
 && apt -qq upgrade -y \
 && apt -qq install -y ocaml libelf-dev ruby-dev rubygems \
 && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* \
 && gem install fpm
