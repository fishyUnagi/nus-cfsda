FROM node:21

WORKDIR /app

COPY package.json .
COPY package-lock.json .
COPY main.js .
COPY public public
COPY views views

RUN npm ci

ENV APP_PORT=3000
ENV INSTANCE_NAME="THIS IS AN INSTANCE_NAME"
ENV INSTANCE_HASH="THIS IS AN INSTANCE HASH"

EXPOSE ${APP_PORT}

ENTRYPOINT node main.js