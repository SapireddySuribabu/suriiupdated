# FROM nginx:stable-alpine

# COPY build /usr/share/nginx/html
# EXPOSE 80
# FROM node:16.3.0-alpine as space
# WORKDIR /app
# COPY . .
# COPY package.json /app
# RUN npm install -g npm@8.13.1
# RUN npm run build

# FROM nginx:stable-alpine
# WORKDIR /app
# COPY --from=space /app/build /usr/share/nginx/html
# EXPOSE 80
# CMD ["npm","start"]
FROM node:8.11-slim

RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app

# copying all the files from your file system to container file system
COPY package.json .

# install all dependencies
RUN npm install

# copy oter files as well
COPY ./ .

#expose the port
EXPOSE 3000

# command to run when intantiate an image
CMD ["npm","start"]