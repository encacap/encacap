# API - NestJS
FROM node:19.6.0-alpine3.17 AS re-api-builder
WORKDIR /usr/src/re-api
COPY package.json yarn.lock ./
RUN yarn install --development --frozen-lockfile
RUN mkdir -p node_modules/.cache && chmod -R 777 node_modules/.cache
COPY . .
CMD ["yarn", "start:dev"]

# Dashboard - ReactJS
FROM node:19.6.0-alpine3.17 AS re-dashboard-builder
WORKDIR /usr/src/re-dashboard
COPY package.json yarn.lock ./
RUN yarn install --development --frozen-lockfile
RUN mkdir -p node_modules/.cache && chmod -R 777 node_modules/.cache
COPY . .
CMD ["yarn", "start"]

# ACBuilding - NextJS
FROM node:19.6.0-alpine3.17 AS re-acbuilding-builder
WORKDIR /usr/src/re-acbuilding
COPY package.json yarn.lock ./
RUN yarn install --development --frozen-lockfile
RUN mkdir -p node_modules/.cache && chmod -R 777 node_modules/.cache
COPY . .
CMD ["yarn", "dev"]
