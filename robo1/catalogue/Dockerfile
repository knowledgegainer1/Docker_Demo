ARG version=18
FROM node:${version}
ARG username=roboshop
RUN useradd ${username}
EXPOSE 8080
WORKDIR /opt/server
COPY package.json /opt/server/
COPY server.js /opt/server/
ENV MONGO=true
RUN npm install 
USER ${username}
CMD ["node", "server.js"]