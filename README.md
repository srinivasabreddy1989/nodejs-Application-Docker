# nodejs-Application-Docker
Example - Dockerizing Node Js application
https://nodejs.org/en/docs/guides/nodejs-docker-webapp/

Get the git URL for the code
Get the instructions from the development team about how they build the application.
Write Dockerfile
FROM node:16
LABEL AUTHOR="hari@javahome.in"
LABEL APP="Web"

# Create app directory
WORKDIR /usr/src/app

COPY package*.json ./
RUN npm install

# Copy appication code
COPY . .

EXPOSE 8080

CMD [ "node", "server.js" ]

