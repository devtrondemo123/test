FROM node:10-slim

WORKDIR /app

RUN npm install -g nodemon

COPY result/package*.json ./

RUN npm ci \
 && npm cache clean --force \
 && mv /app/node_modules /node_modules

COPY result/. .

ENV PORT 80

EXPOSE 80

CMD ["node", "server.js"]
