# Technical Documentation
## 1. What does the `services:` block do?

Think of the services: block as the master blueprint for your app. It's the main section where you list out every single container you want to build—in our case, the database and the web app. Under this block, you define all their individual settings like which Docker image to download, environment variables, ports, and networking rules so Docker knows how to set them up together as a single system.

---

## 2. How did the Nextcloud app container find the database container?
It all comes down to that MYSQL_HOST=database setting. When you use Docker Compose, it automatically sets up a private internal network for your containers and gives them built-in DNS names. Because we named our database service database, Nextcloud didn't need a complicated IP address; it just looked for database on that private network and connected right to it.

---

## 3. What is the difference between `docker run` and `docker-compose up -d`?
* **`docker run`**: This command is used to launch a **single** container manually from the command line. To configure it, you have to type out long, complex commands with inline flags for ports (`-p`), environment variables (`-e`), volume mounts, and custom networks. If you have multiple containers that need to talk to each other, you have to manage and link them manually.
* **`docker-compose up -d`**: This command reads a **declarative YAML file** (`docker-compose.yml`) to orchestrate and spin up **multiple containers simultaneously** in the background (`-d` for detached mode). It automates the creation of networks, manages container dependencies, and makes multi-tier deployments reproducible and easy to scale with a single command.
