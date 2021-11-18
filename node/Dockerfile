FROM node:latest

RUN mkdir -p /usr/src
# RUN mkdir -p /home/node/app/node_modules && chown -R node:node /home/node/app

# RUN npm install nodemon -g

WORKDIR /usr/src

RUN adduser -S node

COPY package*.json .

RUN chown -R node /usr/src

USER node

COPY /src /usr/src

RUN npm install
# RUN npm ci --only=production && npm cache clean --force

# COPY --chown=node:node . .

EXPOSE 5000

#  CMD [ "node", "app.js" ]
CMD ["npm", "run", "start"]
