FROM node:14 AS nodejs

ENV NODE_VERSION 14

RUN node --version \
    && npm version && git --version


RUN which diff2html || npm install -g -ignore-scripts  @nullcc/diff2html-cli || true
RUN which istanbul-merge || npm install -g -ignore-scripts  istanbul-merge || true
RUN npm i -g typescript-language-server && npm install -g typescript && npm install --unsafe-perm -g @nullcc/sdet-cli

