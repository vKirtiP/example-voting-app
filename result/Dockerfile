FROM node:18-slim

WORKDIR /app

RUN npm install -g nodemon

COPY package*.json ./

Run npm ci \
&& npm cachce clean --force \
&& mv /app/node_modules /node_modules


COPY . .

ENV PORT 80

EXPOSE 80

ENTRYPOINT ["/usr/bin/tini","-"]
CMD ["node","server.js"]




