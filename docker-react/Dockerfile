#To run java applications we need to inherit at min a jre
# FROM openjdk:8-jdk-alpine
FROM node:12.16.3 

WORKDIR /new-dir

ENV PORT 80

COPY package.json /new-dir/package.json

RUN npm install

COPY . /new-dir/

ENTRYPOINT [ "npm start" ]
# CMD ["npm start"]