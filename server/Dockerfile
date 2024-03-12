FROM node:14-apline 
WORKDIR /usr/app
COPY ./package.json .
RUN npm i
COPY ./ ./
CMD ["npm", "start"]