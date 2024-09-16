FROM node:14-alpine AS builder

WORKDIR /usr/src/app
COPY . .
#COPY package*.json .
RUN npm install
#ENV REACT_APP_PORT=80
#RUN #npm run start
RUN npm run build #wtf
EXPOSE 80
CMD [ "node", "server.js" ]
#FROM nginx
#
#RUN rm -rf /usr/share/nginx/html/*
#COPY --from=builder /usr/src/app/build /usr/share/nginx/html
#EXPOSE 80
#
#CMD ["nginx","-g","daemon off;"]
