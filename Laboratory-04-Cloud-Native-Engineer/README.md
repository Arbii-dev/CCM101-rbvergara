# Laboratory 04: Cloud-Native Engineer

## Mission Overview
Congratulations! After successfully guiding our clients through multi-cloud evaluations, you have been promoted to the Cloud-Native Engineering Team at CloudNova Technologies. Modern cloud computing is no longer just about renting Virtual Machines (VMs) from AWS or Azure; today's enterprise applications are built using lightweight, portable, and lightning-fast technologies called Containers. Your new mission is to understand the shift from traditional virtualization to containerization by stepping into the shoes of a Cloud-Native Engineer using the KillerCoda Playground to research differences, execute Docker commands, and deploy a live, containerized web server in seconds.

## Mission Objectives
At the end of this laboratory activity, you should be able to:
* Differentiate between traditional Virtual Machines (VMs) and Containers.
* Access a Docker-enabled cloud environment using KillerCoda.
* Execute fundamental Docker CLI (Command Line Interface) commands.
* Pull, run, manage, and terminate a containerized application (Nginx).
* Create professional technical documentation of container operations using Markdown.
* Continue developing a well-organized GitHub Cloud Computing Portfolio.

## Docker Commands Executed

### Checkpoint 3: Verify Installation
* `docker --version` — Checks the installed version of the Docker engine.
* `docker info` — Displays system-wide information regarding the Docker environment status.

### Checkpoint 4: Deploy Your First Container
* `docker pull nginx` — Downloads the official Nginx web server image from Docker Hub.
* `docker run -d -p 8080:80 --name my-web-server nginx` — Runs the Nginx container in detached mode (`-d`), mapping host port 8080 to container port 80.
* `curl http://localhost:8080` — Sends a local HTTP request to verify the web server responds with the expected HTML.

### Checkpoint 5: The Container Lifecycle
* `docker ps` — Lists all currently active, running containers.
* `docker stop my-web-server` — Gracefully stops the specified running container.
* `docker ps -a` — Lists all containers (running and stopped) to verify the status change.
* `docker rm my-web-server` — Permanently removes the stopped container instance from storage.

## Skills Learned
* Gained practical understanding of why containers are more lightweight, boot faster, and consume fewer resources than traditional VMs by sharing the host OS kernel.
* Learned basic container deployment, network port forwarding, and lifecycle management via the Docker command-line interface.
* Learned to validate containerized services locally using `curl` and document operational workflows cleanly.

## Challenges Encountered
* **Port Mapping Understanding:** Ensuring that external traffic on host port `8080` correctly routes to internal container port `80` without conflicting with existing services.
* **Lifecycle State Management:** Keeping track of container states (running vs. exited) to ensure clean workspace habits before removing and cleaning up instances.
