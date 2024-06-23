FROM node:latest as build

WORKDIR /usr/local/app

COPY ./ /usr/local/app/

RUN npm install && npm run build

FROM nginx:latest

COPY --from=build /usr/local/app/dist/client /usr/share/nginx/html

# Expose port 80
EXPOSE 80
