# Introduction to Docker and Building Docker Images

Docker is a popular open-source platform for developing, shipping, and running applications. It provides an easy way to package applications into containers that can be run on any system with the Docker Engine installed. This lab will provide an introduction to Docker and guide you through the process of building your own Docker images.

## What is Docker?

Docker is a containerization platform that allows you to package your application into a container image. A container image is a lightweight, stand-alone, executable package of software that includes everything needed to run an application: code, runtime, system tools, system libraries and settings.

Containers are isolated from each other and bundle their own software, libraries and configuration files; they can communicate with each other through well-defined channels. All containers are run by a single operating system kernel and are thus more lightweight than virtual machines.

## Benefits of Using Docker

1. Portability: You can easily move your application from one environment to another without having to worry about compatibility issues or dependencies.
2. Scalability: You can quickly scale up or down your application depending on the load it needs to handle.
3. Security: Containers provide an additional layer of security as they are isolated from each other and the host operating system.

## Prerequisites

Before you begin this lab you should have some basic understanding of Linux command line tools such as `docker`, `docker-compose` and `docker-machine`. Additionally, you should have access to a Linux machine with the latest version of Docker installed on it.

## Exercise 1 - Building Your First Image

In this exercise we will build our first docker image using the `docker build` command. We will use a simple NodeJS web server as our example application for this exercise:

```javascript
const http = require("http");

const hostname = "127.0.0.1";
const port = 3000;

const server = http.createServer((req, res) => {
  res.statusCode = 200;
  res.setHeader("Content-Type", "text/plain");
  res.end("Hello World\n");
});

server.listen(port, hostname, () => {
  console.log(`Server running at http://${hostname}:${port}/`);
});
```

To build our image we will need two files - a `Dockerfile` which contains instructions for building our image and an `index.js` file which contains our NodeJS web server code (as shown above). Create these two files in the same directory on your Linux machine then open up the `Dockerfile` in your text editor of choice (e.g., vim). Add the following lines to it:

```
FROM node:latest
```

This line tells docker which base image we want to use for our own custom image - in this case we are using the latest version of NodeJS available on docker hub (https://hub.docker/com/_/node).

Next add these lines to your `Dockerfile`:

`WORKDIR /app COPY indexjs . CMD ["node", "indexjs"]`

The first line sets the working directory for our container inside which all subsequent commands will be executed - in this case it's set to `/app`. The second line copies our NodeJS web server code into this directory while the third line tells docker what command it should execute when running our container (in this case it's running our NodeJS web server).

Now that we have written out instructions for building our image save them in your `Dockerfile`. We can now build our image using the following command:

`docker build -t my_image .`

This command tells docker to build an image called “my_image” based on instructions contained within the current directory (denoted by “ . ” at the end). If successful you should see output similar to this:

`Successfully built <image_id> Successfully tagged my_image`
