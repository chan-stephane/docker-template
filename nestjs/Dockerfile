FROM node:20-alpine

RUN apk update && apk add git
RUN git clone https://github.com/nestjs/typescript-starter.git myapp
WORKDIR /myapp
RUN npm i

EXPOSE 3000

CMD [ "npm", "start" ]


