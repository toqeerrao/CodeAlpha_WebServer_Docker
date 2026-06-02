# CodeAlpha: Web Server Deployment using Docker

## Project Overview
This repository contains the complete submission for the **Web Server Deployment** task under the CodeAlpha Internship. The primary objective of this project is to successfully configure, containerize, and deploy a high-performance **Nginx Web Server** inside an isolated environment using **Docker**, ensuring seamless traffic routing from the host machine.

## Tech Stack & Tools Used
* **Containerization Engine:** Docker Desktop
* **Web Server Configuration:** Nginx (Official Image)
* **Version Control System:** Git & GitHub
* **Host Environment:** Windows
## Step-by-Step Implementation & Documentation
## Prerequisites
Ensure that the container runtime system is initialized and available on your environment terminal:
``bash
docker --version
docker pull nginx:latest
docker run -d -p 8080:80 --name myweb nginx
Command Parameter Breakdown:
-d (Detached Mode): Runs the container in the background, allowing the terminal to remain free.

-p 8080:80 (Port Forwarding): Maps port 8080 of your local host machine to the default internal port 80 inside the Docker container.

--name myweb (Naming): Assigns a custom name (myweb) to the container for easier management.

nginx: Specifies the base image to build and launch the container from.
 Verification & Post-Deployment Testing
 Accessing the Live Web Server
Once the container status is active, you can access the hosted Nginx welcome page by navigating to the following address in your web browser:

 URL: http://localhost:8080

 Useful CLI Diagnostics Commands
To inspect the operational status of your running containers:
docker ps
docker logs myweb
Project Demonstration & Visual Proofs
Below are the documented screenshots confirming the successful execution of the project:

1. Live Web Server Output (Browser Verification)
The default Nginx landing page rendering properly at localhost:8080:

2. Version Control & Workspace Setup
Proof of local setup, environment initialization, and tracking configurations:
 Lifecycle Management (Cleanup Guide)
If you need to stop the deployment and cleanly remove the container from your host machine, execute these commands:
# 1. Stop the running container
docker stop myweb

# 2. Delete the container instance
docker rm myweb

