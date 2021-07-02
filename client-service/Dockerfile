FROM node:15-alpine3.10 as build
ENV NODE_ENV production
LABEL version="1.0"
LABEL description="This is the base docker image for prod frontend react app."

WORKDIR /usr/src/app

COPY package*.json yarn.lock ./

RUN yarn install

COPY . ./

RUN yarn build


# production environment
FROM nginx:1.19.10-alpine
COPY --from=build /usr/src/app/build /usr/share/nginx/html

COPY --from=build usr/src/app/nginx/nginx.conf /etc/nginx/conf.d/default.conf
EXPOSE 80
EXPOSE 443
CMD ["nginx", "-g", "daemon off;"]