FROM node:18
EXPOSE 8080
WORKDIR /opt/server
ENV mongo=true
COPY package.json /opt/server/
COPY server.js /opt/server/
RUN npm install
CMD [ "node","server.js" ]