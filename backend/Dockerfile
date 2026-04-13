FROM node:21 AS builder

WORKDIR /app

COPY . .

RUN npm install

FROM node:21-slim

WORKDIR /app

COPY --from=builder /app .

COPY .env.sample .env

EXPOSE 8080

CMD ["npm", "start"]
