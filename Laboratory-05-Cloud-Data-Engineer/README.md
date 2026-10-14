# Laboratory 05 - Cloud Data Engineer

## Mission Overview

Congratulations! Your seamless deployment of containerized web servers has caught the attention of the senior architects. You have now been temporarily reassigned to the Cloud Data Engineering Team at CloudNova Technologies.

In the cloud, data is everything. However, not all data is stored the same way. While traditional computers use hard drives (Block Storage) and shared network drives (File Storage), modern cloud applications rely heavily on Object Storage to store massive amounts of unstructured data like images, videos, and backups. The industry standard for this is Amazon S3, but today, you will deploy your very own S3-compatible cloud storage server using an open-source tool called MinIO.

Using your KillerCoda Playground, you will combine your new Docker skills with your cloud storage knowledge to deploy a live object storage server, create a storage "bucket," and upload data over the web.

Remember: A cloud engineer doesn't just store data; they ensure it is scalable, accessible, and secure.

## Objectives

At the end of this laboratory activity, you should be able to:

- Differentiate between Block, File, and Object Storage.
- Deploy an S3-compatible Object Storage server (MinIO) using Docker.
- Access a cloud service via a web interface using port forwarding.
- Create a storage bucket and upload objects (files) to the cloud.
- Document cloud storage operations using Markdown.
- Continue expanding a professional GitHub Cloud Computing Portfolio.

## Tools Used

- **KillerCoda Ubuntu Playground:** cloud-based Linux environment for the lab
- **Docker:** container runtime used to deploy the storage server
- **MinIO:** open-source, S3-compatible object storage server
- **MinIO Web Console (port 9001):** browser interface for creating buckets and uploading objects
- **Markdown:** used to document the deployment
- **Git and GitHub:** used to publish the work to my Cloud Computing Portfolio

## Skills Learned

- Distinguishing Block, File, and Object Storage and knowing when each is used
- Deploying a containerized storage service with `docker run`, including port mapping (`-p`), naming (`--name`), and detached mode (`-d`)
- Configuring a service with environment variables (`-e`) to set the root user and password
- Verifying a running container with `docker ps`
- Accessing a cloud service through a web interface using port forwarding
- Creating a storage bucket (`client-photos`) and uploading objects through a web console
- Troubleshooting container image pull errors and finding an alternative image source
- Documenting cloud operations in Markdown
- Building a professional GitHub portfolio
