FROM node:16 
# as base

RUN mkdir -p /usr/app/src
# RUN mkdir -p /home/node/app/node_modules && chown -R node:node /home/node/app


WORKDIR /usr/app/src

# COPY /src/package*.json .

COPY . /usr/app/src

# FROM base as production
# ENV NODE_ENV=production
# RUN npm ci --only=production && npm cache clean --force
# CMD ["node", "bin/www"]


# FROM base as dev
# ENV NODE_ENV=development
RUN npm install -g nodemon && npm install


RUN adduser --system --group app

RUN chown -R app /usr/app/src
# COPY --chown=app:app . .

USER app


EXPOSE 3000

# CMD ["npm", "run", "start"]
CMD ["nodemon", "bin/www"]
