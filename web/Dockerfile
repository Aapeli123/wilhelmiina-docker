FROM node as build-stage
WORKDIR /app
RUN git clone https://github.com/Aapeli123/wilhelmiina-web
WORKDIR /app/wilhelmiina-web
RUN yarn install
RUN yarn run build
FROM nginx
RUN rm /etc/nginx/conf.d/default.conf
COPY ./nginx/nginx.conf /etc/nginx/conf.d/default.conf
COPY --from=build-stage /app/wilhelmiina-web/build/ /var/www/wilhelmiina