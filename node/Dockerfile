FROM node:alpine

WORKDIR /srv/app

# RUN npm install --global pm2

COPY ./package*.json ./

RUN npm install
# RUN npm install --production

COPY ./ ./

RUN npm run build

EXPOSE 3000

USER node

CMD ["npm", "run", "dev"]
# CMD [ "pm2-runtime", "npm", "--", "start" ]