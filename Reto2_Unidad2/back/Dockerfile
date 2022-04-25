FROM node:16-alpine
ENV NODE_ENV = 'production'
ENV PORT = 5000
ENV URL_DB_CONNECTION = 'mongodb://172.31.10.25:27017/bookstore'
WORKDIR /usr/src/app
COPY package*.json ./
RUN npm install
COPY . .
RUN node createBook.js
EXPOSE 5000
CMD [ "node", "server.js" ]