FROM node:15.0.1-alpine3.10

WORKDIR /app

COPY package.json yarn.lock /app/

RUN yarn install --network-timeout 500000

COPY . /app

RUN yarn run build

EXPOSE 3001

CMD ["yarn", "start:prod"]