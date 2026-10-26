# Laboratory 6: The Cloud Deployment Engineer

## Mission Overview
Congratulations! Your flawless work in deploying data storage solutions has earned you a spot on the Cloud Deployment Team at CloudNova Technologies.

Up until now, you have been deploying single containers (like a standalone web server or a storage bucket). However, real-world enterprise applications are rarely just one container. They are "multi-tier" systems that require a frontend web application communicating seamlessly with a backend database. Deploying these one by one manually is prone to error.

Enter Docker Compose. In this mission, you will transition from manual commands to Infrastructure as Code (IaC). Using a YAML configuration file, you will define a multi-container private cloud storage application (Nextcloud and MariaDB) and deploy the entire stack simultaneously with a single command!

Remember: A junior engineer deploys servers by typing commands; a senior engineer deploys infrastructure by writing code.

## Objectives
At the end of this laboratory activity, you should be able to:
* Explain the concept of a multi-tier application architecture.
* Understand the purpose and structure of a docker-compose.yml file.
* Use a Linux command-line text editor (nano) to create configuration files.
* Deploy a multi-container application (Nextcloud + Database) using Docker Compose.
* Document deployment procedures and Infrastructure as Code (IaC) principles using Markdown.
* Continue expanding your professional GitHub Cloud Computing Portfolio.

## Skills Learned
* Splitting Up the Heavy Lifting: Figuring out how to properly separate your user-facing web app from your persistent database so one crash doesn't take down the other.

* Writing Infrastructure as Code: Trading messy, manual terminal commands for a clean, reproducible YAML file that builds your whole environment automatically.

* Letting Docker Handle the Networking: Letting Docker Compose spin up private internal networks and bridge everything together behind the scenes without having to wire IP addresses manually.

* Managing the Full Container Lifecycle: Knowing how to spin up stacks, check logs, verify active ports in a browser, and tear everything down cleanly when you're done.

## Commands Executed
```bash
# 1. Create and navigate into the project directory
mkdir nextcloud-deployment
cd nextcloud-deployment

# 2. Create and write the Docker Compose configuration file
nano docker-compose.yml

# 3. Deploy the multi-container stack in the background
docker-compose up -d

# 4. Check that both containers are up and running smoothly
docker ps

# 5. Gracefully stop and clean up the entire stack
docker-compose down
