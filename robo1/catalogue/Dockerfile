FROM node:18
RUN useradd roboshop
USER roboshop
WORKDIR /app
ADD https://roboshop-builds.s3.amazonaws.com/catalogue.zip /app/catalogue.zip
RUN unzip /app/catalogue.zip 
RUN cd /app/catalogue
RUN rm /app/catalogue
RUN mv /app/catalogue/* /app/
RUN npm install 
COPY catalogue.service /etc/systemd/system/catalogue.service
COPY mongo.repo /etc/yum.repos.d/mongo.repo
RUN dnf install mongodb-org-shell -y
CMD ["node", "app.js"]