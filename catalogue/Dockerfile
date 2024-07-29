FROM node:18
WORKDIR /opt/server
EXPOSE 8080
COPY server.js   /opt/server/
COPY package.json  /opt/server/
RUN npm install
CMD ["node", "server.js"]