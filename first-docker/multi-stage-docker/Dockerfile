##########################################
# 04. Multi-Stage Build Dockerfile (React)
##########################################

FROM node:20-alpine as build
WORKDIR /app
COPY python*.json ./
RUN npm install
COPY . .
RUN npm build

FROM nginx:alpine
COPY --from=build /app/build /usr/share/nginx/html
EXPOSE 80
CMD [ "nginx", "-g", "daemon off" ]