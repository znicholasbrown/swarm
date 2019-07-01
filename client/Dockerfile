# Light version of Linux to run Node ~50mb
FROM node:8.16.0-alpine

RUN mkdir -p /srv/client
WORKDIR /srv/client

# Wildcard gets package.json && package-lock.json
COPY package*.json /srv/client/
RUN npm install

# Copy local code to the container
COPY . /srv/client/

# Start the server
CMD ["npm", "start"]