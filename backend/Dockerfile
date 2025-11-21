FROM node:20
EXPOSE 8080
ENV DB_HOST=mysql
RUN useradd expense
RUN mkdir /opt/server 
RUN chown expense:expense -R /opt/server
WORKDIR /opt/server
COPY package.json .
COPY *.json /opt/server/
RUN npm install
CMD [ "node","index.js" ]
