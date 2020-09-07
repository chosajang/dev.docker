# Dockerfile
FROM node:latest
MAINTAINER CHOSAJANG jonny@chosajang.com

RUN mkdir /app
ADD . /app
WORKDIR /app

RUN npm install

ENV NODE_ENV=production

CMD ["node", "index.js"]