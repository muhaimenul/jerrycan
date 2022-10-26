FROM node:18
# ENV NODE_ENV=development

RUN mkdir -p /usr/app

WORKDIR /usr/app

# Copy app files
# COPY /src/package*.json .
COPY . /usr/app

RUN adduser --system --group app

RUN chown -R app /usr/app/src

USER app

# Expose port
EXPOSE 3000

# Start the app
CMD ["npm", "run", "start"]
