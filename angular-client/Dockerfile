FROM node:alpine AS builder

WORKDIR /app

COPY . .

RUN npm install

COPY . .

EXPOSE 4200

CMD npm run start