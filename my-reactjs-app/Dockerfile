FROM node:14-alpine AS builder
WORKDIR /app
COPY . .
RUN npm run build

FROM nginx:1.19-alpine AS server
COPY --from=builder ./app/build /usr/share/nginx/html