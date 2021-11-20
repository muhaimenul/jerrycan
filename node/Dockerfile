FROM node:16

RUN mkdir -p /usr/app/src
# RUN mkdir -p /home/node/app/node_modules && chown -R node:node /home/node/app

# RUN npm install nodemon -g

WORKDIR /usr/app/src


COPY package*.json .

COPY . /usr/src

RUN npm install -g nodemon && npm install

RUN adduser --system --group app

RUN chown -R app /usr/app/src

USER app


# RUN npm ci --only=production && npm cache clean --force

# COPY --chown=node:node . .

EXPOSE 3000

# CMD [ "node", "bin/www" ]
# CMD ["npm", "run", "start"]
CMD ["nodemon", "bin/www"]
