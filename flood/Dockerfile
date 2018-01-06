FROM node:7.8.0

RUN apt-get update && apt-get install -y mediainfo git && rm -rf /var/lib/apt/lists/*

RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app
RUN git clone https://github.com/jfurrow/flood.git .
COPY config.docker.js /usr/src/app/config.js

# RUN npm install && npm cache clean --force

# RUN npm build

EXPOSE 3000
VOLUME ["/data"]

# CMD ["npm", "start"]