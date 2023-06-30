FROM node:16-alpine

RUN mkdir -p /SistemaInventarioBE/node_modules && chown -R node:node /SistemaInventarioBE
WORKDIR /SistemaInventarioBE

USER node
COPY --chown=node:node package.json package-lock.json* ./

RUN npm install

COPY --chown=node:node . .

EXPOSE 2087

CMD [ "npm", "start" ]