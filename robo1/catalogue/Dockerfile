FROM node:18
RUN useradd roboshop
USER roboshop
WORKDIR /app
ADD https://roboshop-builds.s3.amazonaws.com/catalogue.zip   /app/catalogue
WORKDIR /app/catalogue 
RUN mv /app/catalogue/* /app
WORKDIR /app
RUN npm install 
COPY catalogue.service /etc/systemd/system/catalogue.service
COPY mongo.repo /etc/yum.repos.d/mongo.repo
RUN dnf install mongodb-org-shell -y
CMD ["node", "app.js"]