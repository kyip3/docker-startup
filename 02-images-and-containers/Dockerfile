# To create a custom image, we first use a base image
FROM node

#tell docker that all docker command execute inside the folder
WORKDIR /app 

# copy outside all files into this image root folder
# it will copy all files except Dockerfule
#COPY . .

# copy outside all files into this image /app folder
# /app will be created if is not found
# you can also use COPY . ./ (as a relative file, cause the WORKDIR is set)
COPY . /app

#by default, all command will run in rool folder, e.g COPY . . 
# so we need specify WORKDIR /app at the top
RUN npm install

#cannot execute this, as every time it build it will run this cmd
#RUN node server.js

# container start, expose 80 to our local
EXPOSE 80

#this will only run when the container is started.
#not when a image is build
CMD ["node", "server.js"]