FROM node:19.6.0-alpine3.17 AS re-api-builder

WORKDIR /usr/src/re-api

COPY package.json yarn.lock ./

RUN yarn install --development --frozen-lockfile

COPY . .

CMD ["yarn", "start:dev"]