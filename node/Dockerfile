FROM node:18
# ENV NODE_ENV=development

RUN mkdir -p /usr/src/app

WORKDIR /usr/src/app

# Copy app files
# COPY /src/package*.json .
COPY ./src/package*.json ./

COPY ./src .

RUN adduser --system --group app

RUN chown -R app /usr/src/app

USER app

WORKDIR /usr/src/app

RUN npm install

# Expose port
EXPOSE 3000

# Start the app
CMD ["npm", "start"]
