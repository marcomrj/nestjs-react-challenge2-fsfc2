FROM node:12.14.0-alpine3.11

WORKDIR /app

ENV PATH /app/node_modules/.bin:$PATH

COPY package.json ./
COPY package-lock.json ./
RUN npm i

COPY . ./

ENV  REACT_APP_API_URL  http://localhost:3000

CMD ["npm", "start"]