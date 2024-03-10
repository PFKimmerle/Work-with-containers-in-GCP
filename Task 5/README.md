# Task 5: Publishing Docker Images to Google Artifact Registry

## Overview

Publishing Docker images to Google Artifact Registry allows distribution and deployment of your applications across environments. This task demonstrates how to push a Docker image to Artifact Registry and then pull and run the image to ensure it's accessible.

## Prerequisites

- Docker image created in Task 2.
- Access to Google Cloud Platform (GCP) and Artifact Registry enabled on your GCP project.

## Steps to Publish Docker Images

### 1. Tagging Your Docker Image

Tag your Docker image with the registry name to push it to Google Artifact Registry.

- **Command**: `docker tag node-app:0.2 us-central1-docker.pkg.dev/<PROJECT_ID>/my-repository/node-app:0.2`
  - Replace `<PROJECT_ID>` with your actual GCP project ID.

### 2. Configuring Docker for Google Cloud Authentication

Ensure Docker can authenticate with Google Cloud.

- **Command**: `gcloud auth configure-docker us-central1-docker.pkg.dev`

### 3. Pushing the Image to Artifact Registry

Push your tagged image to Google Artifact Registry.

- **Command**: `docker push us-central1-docker.pkg.dev/<PROJECT_ID>/my-repository/node-app:0.2`

### 4. Pulling and Running the Image from Artifact Registry

Verify the image is accessible by pulling and running it.

- **Commands**:
  - `docker pull us-central1-docker.pkg.dev/<PROJECT_ID>/my-repository/node-app:0.2`
  - `docker run -p 8080:80 -d us-central1-docker.pkg.dev/<PROJECT_ID>/my-repository/node-app:0.2`

### Validating the Deployment

After running the container, access it through your browser or use `curl` to verify the application responds as expected.

## Understanding the Process

- **Tagging** prepares your Docker image for the registry by associating it with a specific project and repository in Google Cloud.
- **Authentication** ensures your Docker client can securely communicate with Google Cloud services.
- **Pushing and pulling images** demonstrates the image's lifecycle within the registry, showcasing how you can distribute and access your Docker images.

