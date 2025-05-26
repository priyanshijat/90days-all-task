## Introduction

Docker is a popular tool used in DevOps to make it easier to build, test, and run applications. It helps package an app along with everything it needs—like libraries and settings—into something called a **container**. This makes sure the app runs the same way no matter where you launch it, whether it's on a developer's laptop or a production server.

## What is Docker:- 
Docker is an open-source platform that makes it easier to create, run, and manage applications using containers.

### Why Use Docker?
* Consistency: Works the same on all environments (dev, test, production).

* Isolation: Each container is independent and isolated from others.

* Portability: Containers can run on any system with Docker installed.

* Efficiency: Containers share the host OS, making them more lightweight than virtual machines.

### Virtualization vs. Containerization

**Virtualization** uses virtual machines (VMs) to run multiple systems on one computer. Each VM has its own full operating system, which makes it heavy and slow to start.

**Containerization**, used by tools like Docker, runs applications in containers that share the same operating system. Containers are much lighter and start much faster than VMs.

| Feature            | Virtualization                        | Containerization                      |
|--------------------|---------------------------------------|----------------------------------------|
| Size               | Large (includes full OS)              | Small (shares OS)                      |
| Speed              | Slower to start                       | Starts quickly                         |
| Resource Use       | Uses more memory and CPU              | Uses less memory and CPU               |
| Portability        | Harder to move                        | Easy to move and run anywhere          |

### Why Containers Are Better for Microservices and CI/CD

Containers work really well for **microservices** because each service can run in its own container. This makes it easier to update, test, and scale each part of an app separately. In **CI/CD pipelines**, containers make the process faster and more reliable by ensuring the app runs the same way at every step—from coding and testing to deployment. That’s why containerization is the preferred choice in modern DevOps.

### Components of Docker:-
1) ## Docker Engine
Docker Engine is the core software that enables Docker to run containers. It’s the client-server application that manages the lifecycle of containers.

🔹 Components of Docker Engine
a) Docker Daemon (dockerd)

  * The background service running on the host OS.
  * Responsible for:

      * Creating and managing Docker images, containers, networks, and volumes.

     * Communicating with other Docker daemons (in a cluster setup like Swarm).
  
b) Docker CLI (docker)
    * The command-line interface used by developers/admins to interact with Docker.
c) REST API
   *  The interface that allows the Docker CLI or other tools to interact with the Docker daemon programmatically.

2) ### Dockerfile:-
A Dockerfile is a text file that contains a set of instructions for building a Docker image. It tells Docker how to assemble an image step by step.

##  Why Use a Dockerfile?
Instead of building containers manually, you write a Dockerfile so Docker can:

  * Automate the image creation process

  * Ensure consistency

  * Easily share and version your environment

```
# Use an official Node.js base image
FROM node:18

# Set the working directory inside the container
WORKDIR /app

# Copy package.json and install dependencies
COPY package*.json ./
RUN npm install

# Copy the rest of the app code
COPY . .

# Expose port 3000
EXPOSE 3000

# Define the command to run the app
CMD ["node", "index.js"]
```
##  How to Use a Dockerfile?
Create a Dockerfile in your project folder.

Build the image:

```
docker build -t my-app .
#Run a container from it:


docker run -p 3000:3000 my-app
```

3) ### 🧱 What is a Docker Image?
   A Docker image is a read-only blueprint or template used to create Docker containers. It includes:

   * The application code

   * System libraries

   * Dependencies

   * Configuration files

   * Environment settings

Basically, everything needed to run an application.
  
  ##  How is an Image Created?
You create a Docker image using a Dockerfile with the command:

```
docker build -t my-app .
```

4) ### 🌐 What is Docker Hub?
Docker Hub is a cloud-based registry service provided by Docker where you can:

   * Find, share, and store Docker images

   * Publish your own images (public or private)

   * Pull pre-built images to run containers quickly

   * Think of Docker Hub as the GitHub for Docker images.

### Common Commands
Pull an image from Docker Hub:

```
docker pull nginx
Push an image to Docker Hub:
```

```
docker tag my-app username/my-app
docker push username/my-app
Login to Docker Hub:
```
```
docker login
🔹 URL
```
