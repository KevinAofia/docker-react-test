FROM node:12.16.3
WORKDIR /new-dir
ENV PORT 80
COPY package.json /new-dir/package.json
RUN npm install
COPY . /new-dir
ENTRYPOINT ["npm start"]