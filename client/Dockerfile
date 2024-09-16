FROM node:14-alpine AS builder

WORKDIR /usr/src/app
COPY . .

RUN npm install

RUN npm run build
EXPOSE 80
CMD [ "npm", "run", "start_docker_dev" ]

