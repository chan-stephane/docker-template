FROM node:20-alpine

WORKDIR /app

# use --typescript if you want to use ts
RUN npx create-docusaurus@latest my-website classic --javascript
WORKDIR /app/my-website
RUN npm i


# EXPOSE 3000

# CMD [ "pm2-runtime", "start", "bin/www" ]


