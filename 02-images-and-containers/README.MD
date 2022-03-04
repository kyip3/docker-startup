# Images and Containers

## Images 
blue prints and application codes

## Containers
running instances of those images

## Example 1 (Building on pre-build image)

### 1. Node Images
- We can use an existing pre-build image, that can be downloaded from docker hub.
https://hub.docker.com/_/node

- This image contains setup code, environment setup and also node installation

### 2. Run the cmd to download the lastest node image from docker hub to our local docker machine

```
docker run node
```

### 3. List all the processes 

```
docker ps -a
```
- You will notice that there is a new image created under 'node'


### 4. Run the image
Run and expose an interactive session inside the container (-it flag)
```
docker run -it node
```

### 5. Run basic node command
```
1+1
```
It will return 2. You can also run other node command in there.


### 6. To quit, enter Ctrl+C twice.

### 7. List all the processes again
```
docker ps -a
```
- You will notice that there is a another new container id created.
- Each time you run a image, there will be a new container id.


## Example 2 (Building a custom image)

### 1. Npm install packages in local
Notice that package-lock.json and node_modules are created
```
npm install
```

### 2. load localhost port 80
http://localhost/
A simple app will be loaded

### 3. create a Dockerfile 

### 4. Build the docker image
```
docker build .
```

### 5. Run the docker image
Specify local port 3000 and docker container internal exposed port 80
```
docker run -p 3000:80 19050991285e
```

### 6. List the processes and stop
```
docker ps
docker stop angry_lamport
```

- If you run 'docker ps', it doesnt list there anymore 
- Run 'docker ps -a' instead.
```
docker ps -a
```

keynotes:

<img width="888" alt="Screenshot 2022-03-04 at 10 39 03 PM" src="https://user-images.githubusercontent.com/12857531/156783190-e47a1cd5-bc43-4a8e-8502-dd8a47fd0626.png">

