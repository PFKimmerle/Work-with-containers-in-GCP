# Task 3: Running a Docker Container

## Overview

This task focuses on taking a Docker image and running it as a container on a specified port. 

## Prerequisites

- Successful completion of Task 2: Building a Docker Image for a Simple Node Application.
- A Docker image of your Node.js application ready to be run.

## Steps to Run the Docker Container

### 1. Prepare the Environment

Ensure that Docker is running on your system and that you have an image ready to be deployed as a container.

### 2. Running the Container

Utilize the `docker run` command to start a container from your image. You will map a host port to a container port to make the application accessible.

- **Command**: `docker run -p 4000:80 --name my-node-app -d node-app:0.1`
  - `-p 4000:80` maps port 4000 on the host to port 80 on the container.
  - `--name my-node-app` assigns the name "my-node-app" to your running container.
  - `-d` runs the container in detached mode, allowing it to run in the background.
  - `node-app:0.1` is the name and tag of your Docker image.

### 3. Verify the Running Container

To ensure that your container is running as expected, use the `docker ps` command. It should list your container with the status "Up".

- **Command**: `docker ps`

### 4. Accessing the Application

Open a web browser and navigate to `http://localhost:4000`. You should see the "Hello World" message served by your Node.js application.

### 5. Viewing Container Logs

If you wish to view the logs produced by your container (useful for debugging), execute the `docker logs` command followed by your container's name or ID.

- **Command**: `docker logs my-node-app`

## Understanding Container Deployment

Running your Docker image as a container and making it accessible via a web port is a foundational skill in Docker-based application deployment. It enables you to deploy scalable, isolated applications quickly.
