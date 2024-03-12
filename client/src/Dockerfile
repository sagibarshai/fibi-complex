FROM node:14-apline as builder
WORKDIR /usr/app
COPY ./package.json .
RUN npm i
COPY ./ ./
RUN npm run build

from nginx
EXPOSE 3000
COPY --from=builder /usr/app/build /usr/share/nginx/html
COPY ./nginx/default.conf etc/nginx/conf.d/default.conf