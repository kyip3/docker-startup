#use node js 14 as base image
FROM node:14

#working directory called app,
WORKDIR /app

#copy the file into that directory
COPY package.json .

#do a npm install to pull node modules lib
RUN npm install

#copy the files after installing
COPY . .

#expose port 3000 to outside world
EXPOSE 3000

#execute app.mjs with node command.
CMD [ "node", "app.mjs" ]