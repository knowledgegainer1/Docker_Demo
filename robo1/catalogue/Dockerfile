FROM node:18
RUN useradd roboshop
USER roboshop
WORKDIR /app
RUN wget -O /app/catalogue.zip https://roboshop-builds.s3.amazonaws.com/catalogue.zip 
RUN unzip /app/catalogue.zip 
WORKDIR /catalogue/
COPY /* /app/

RUN npm install 
COPY catalogue.service /etc/systemd/system/catalogue.service
COPY mongo.repo /etc/yum.repos.d/mongo.repo
RUN dnf install mongodb-org-shell -y
CMD ["node", "app.js"]