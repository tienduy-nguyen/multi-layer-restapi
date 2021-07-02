
FROM node:15-alpine3.10
ENV NODE_ENV production
LABEL version="1.0"
LABEL description="This is the base docker image for Humaine frontend react app."

WORKDIR /usr/src/app

COPY package*.json yarn.lock ./

RUN yarn install

COPY . ./

COPY --chown=node:node . .

USER node

EXPOSE 4000

CMD "yarn" "start"
