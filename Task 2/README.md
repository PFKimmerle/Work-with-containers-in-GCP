# Task 2: Building a Docker Image for a Node Application

## Overview

This task is how to create a Docker image for a Node.js application that outputs "Hello World" when accessed. This step is fundamental in deploying applications with Docker, facilitating easy distribution and scalability.

## Prerequisites

- Completion of Task 1: Hello World.
- Docker installed on your local machine or access to a Docker environment like Google Cloud Shell.
- Basic familiarity with Docker commands and workflows.
- Understanding of Node.js (optional but beneficial).

## Steps to Build and Run the Node Application Container

### 1. Prepare the Environment

Ensure Docker is installed and running on your system.

### 2. Create a Project Directory

Create and navigate into a new directory for your project. This directory will hold your Dockerfile and Node.js application code.

### 3. Develop the Dockerfile

In the project directory, create a Dockerfile with the necessary instructions for building your Docker image. This includes setting up the Node.js environment, copying your application code, and defining the command to run your app.

### 4. Write the Node.js Application

Create a simple Node.js app that establishes an HTTP server. The server should listen on a designated port and respond with "Hello World" to any requests.

### 5. Build the Docker Image

Utilize the `docker build` command to generate your Docker image from the Dockerfile. Tag this image with a version number for easier management.

### 6. Verify the Image Creation

List all the Docker images using `docker images` to ensure your new image is created and tagged correctly.

### 7. Run Your Container

Start a container from your image. It will run in the background, serving your "Hello World" application on the defined port.

### 8. Access the Application

Open a web browser and navigate to the Docker host's IP address at the specified port to see your "Hello World" message.

## Understanding the Docker Process

Creating a Docker image encapsulates your application and its dependencies, making your app easily deployable and scalable across any Docker-supported platform.
