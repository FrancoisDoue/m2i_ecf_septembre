FROM node:14-alpine

WORKDIR /usr/src/app
COPY . .

RUN npm install

#COPY ../.env ./node_modules/.bin

#RUN #npm run build
RUN #./node_modules/.bin/env-cmd -e dev react-scripts build
EXPOSE 3000
CMD [ "yarn", "run", "start" ]

