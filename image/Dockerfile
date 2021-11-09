FROM node:14 AS nodejs

ENV NODE_VERSION 14

# RUN groupadd --gid 1000 node \
#   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node

# COPY --from=nodejs /usr/local/bin/node /usr/local/bin/
# COPY --from=nodejs /usr/local/lib/node_modules /usr/local/lib/node_modules
# COPY --from=nodejs /opt/ /opt/

# RUN ln -sf /usr/local/bin/node /usr/local/bin/nodejs \
#   && ln -sf ../lib/node_modules/npm/bin/npm-cli.js /usr/local/bin/npm \
#   && ln -sf ../lib/node_modules/npm/bin/npx-cli.js /usr/local/bin/npx \
#   && ln -sf /opt/yarn*/bin/yarn /usr/local/bin/yarn \
#   && ln -sf /opt/yarn*/bin/yarnpkg /usr/local/bin/yarnpkg
# Show version
RUN node --version \
    && npm version && git --version

RUN which diff2html || npm install -g -ignore-scripts  @nullcc/diff2html-cli || true
RUN which istanbul-merge || npm install -g -ignore-scripts  istanbul-merge || true