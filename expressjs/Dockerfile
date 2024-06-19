FROM node:20-alpine

WORKDIR /app

RUN npm init -y
RUN npm install express
RUN npm install pm2 -g
RUN pm2 install pm2-logrotate
RUN pm2 set pm2-logrotate:dateFormat YYYY-MM-DD_HH-mm-ss
RUN pm2 set pm2-logrotate:rotateInterval 0 0 0 * *
RUN pm2 set pm2-logrotate:rotateModule true

EXPOSE 3000

CMD [ "pm2-runtime", "start", "app.js" ]


