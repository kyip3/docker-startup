**Demo to test run docker**

## 1. Build the docker file:

What it does?
Download node:14 image, and execute the instructions in Dockerfile

```
docker build .
```

## 2. Find the docker image id

```
docker images
```

## 3. Run docker by specifying the image id

```
docker run -p 3000:3000 4278fac2b045
```

## 4. Access http://localhost:3000/ 

You should see Hi here!

## 5. To stop the container, open a new terminal and list the running container, grab the "NAMES" of the container
```
docker ps
```

# 6. Execute stop command
```
docker stop trusting_solomon
```
