# Docker Container Lifecycle Commands

1. **`docker ps`**
   - Lists all currently running containers, displaying their container ID, image name, status, and port mappings.

2. **`docker stop my-web-server`**
   - Sends a SIGTERM signal to stop the active container named `my-web-server`.

3. **`docker ps -a`**
   - Lists all containers on the system—both running and stopped—to verify that the target container's status has changed to "Exited".

4. **`docker rm my-web-server`**
   - Completely deletes the stopped container instance from disk
