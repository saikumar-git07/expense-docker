FROM node:20.15.0-alpine3.20
EXPOSE 8080
ENV DB_HOST=mysql
RUN adduser expense
RUN mkdir /opt/server 
RUN chown expense:expense -R /opt/server
WORKDIR /opt/server
COPY package.json .
COPY *.json /opt/server/
RUN npm install
CMD [ "node","index.js" ]
