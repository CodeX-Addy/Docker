# stage 1: build stage

FROM node:22-alpine AS build
WORKDIR /app

COPY package*.json ./
RUN npm install
COPY . .

# stage 2: production stage

FROM node:22-alpine
WORKDIR /app

COPY --from=build /app /app
EXPOSE 3000
ENV PORT=3000

CMD ["node", "index.js"]
