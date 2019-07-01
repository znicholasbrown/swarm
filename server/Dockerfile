# Light version of Linux to run Node ~50mb
FROM node:8.16.0-alpine

RUN mkdir -p /srv/server
WORKDIR /srv/server

# Wildcard gets package.json && package-lock.json
COPY package*.json /srv/server/
RUN npm install

# Copy local code to the container
COPY . /srv/server/

# Start the server
CMD ["npm", "run", "server"]