# Task 4: Debugging Docker Containers

## Overview

Debugging is a critical aspect of working with Docker containers. It allows you to understand and fix issues that may occur during the development or deployment of your application. This task covers common debugging practices including viewing logs, inspecting container metadata, and interacting with a running container.

## Prerequisites

- A running Docker container from Task 3.

## Debugging Steps

### 1. Viewing Container Logs

Logs provide vital information about the operations and errors within your container. To view the logs:

- **Command**: `docker logs <container-name-or-id>`
  - Replace `<container-name-or-id>` with your container's name or ID.

### 2. Inspecting Container Metadata

Docker inspect provides detailed information about your container's configuration and state.

- **Command**: `docker inspect <container-name-or-id>`
  - This command returns a JSON output with detailed metadata about your container.

### 3. Running an Interactive Bash Session

To debug issues or inspect the container from within, start an interactive Bash session:

- **Command**: `docker exec -it <container-name-or-id> bash`
  - This allows you to execute commands inside the container as if you were working on a local Bash session.

### Tips for Effective Debugging

- **Follow the logs**: Regularly monitor the container logs for errors or unexpected behavior.
- **Use `docker inspect` wisely**: Inspect the container to understand its current state, network settings, and mounted volumes.
- **Interact with the container**: Use `docker exec` to interact with the running container, which is especially useful for troubleshooting and quick fixes.

## Understanding the Debugging Tools

- **`docker logs`** offers a window into the running process, making it invaluable for troubleshooting.
- **`docker inspect`** provides a snapshot of the container's current state, including configuration, network settings, and health.
- **`docker exec`** allows for direct interaction with the container, facilitating real-time debugging and file inspection.
