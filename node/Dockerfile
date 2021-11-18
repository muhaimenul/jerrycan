FROM node:latest

RUN mkdir -p /usr/src

# RUN npm install nodemon -g

WORKDIR /usr/src

COPY package.json .
RUN npm install
COPY . /usr/src