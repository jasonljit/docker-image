# alpine3.9.4, node10.16.3, pm2, mysql, redis-cli
FROM alpine:3.9.4 AS base
RUN apk add redis

FROM node:10.16.3-alpine
COPY --from=base /usr/bin/redis-cli /usr/bin/redis-cli
RUN npm install pm2@3 -g
RUN apk add mysql-client
