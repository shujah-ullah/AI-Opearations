FROM node:18-alpine as prod
ARG PORT=8000
ENV PORT=$PORT
WORKDIR app
copy src src
copy package.json .
RUN npm install --only=prod
EXPOSE $PORT
CMD npm run start:prod

FROM prod as dev
RUN npm install --only=dev
CMD npm start




