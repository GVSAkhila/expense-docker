#Before best practices implemented
# FROM node:20
# EXPOSE 8080
# ENV DB_HOST="mysql"
# RUN mkdir /opt/server
# WORKDIR /opt/server
# COPY package.json .
# COPY *.js .
# RUN npm install
# CMD ["node", "index.js"]
# after best practice

FROM node:20.18.0-alpine3.20
EXPOSE 8080
ENV DB_HOST="mysql"
RUN mkdir -p /opt/server
WORKDIR /opt/server
COPY package.json .
RUN npm install && npm cache clean --force
COPY *.js .
CMD ["node", "index.js"]
