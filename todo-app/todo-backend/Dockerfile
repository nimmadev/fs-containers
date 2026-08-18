FROM node:24-bookworm-slim

WORKDIR /usr/src/app

RUN apt-get update && apt-get install --no-install-recommends dumb-init -y

COPY --chown=node:node ./ ./

RUN npm ci

CMD ["dumb-init", "npm", "start"]