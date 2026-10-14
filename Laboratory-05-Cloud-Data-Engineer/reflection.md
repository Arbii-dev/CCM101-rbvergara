# Mission Reflection

**1. Why is object storage better suited for storing millions of photos than a traditional block storage hard drive?**

Object storage is better suited for millions of photos because it was designed for scale. A traditional block storage drive is tied to a single server, has a fixed capacity, and relies on a hierarchy of folders that becomes harder to manage as files multiply. Object storage keeps each photo as an object in a flat structure with a unique key and metadata, and it grows by adding more nodes instead of replacing drives. It is also accessed over HTTP, so any application can store or retrieve photos without mounting a disk.

**2. How did using Docker make it easier to deploy the MinIO storage server?**

Docker packaged MinIO with everything it needs, so I did not have to install dependencies or configure the server by hand. A single `docker run` command downloaded the image, started the container, mapped the ports, and set the login credentials. If something went wrong, I could remove the container and start again cleanly.

**3. What is a "bucket" in the context of cloud storage?**

A bucket is a top-level container in object storage that holds objects (files). It looks like a folder, but it is flat, has a unique name, and is where settings and access permissions are applied. My bucket was named `client-photos`.

**4. How do large enterprise companies ensure their object storage data is not lost if the physical server crashes?**

I think enterprises protect against server crashes through redundancy. Objects are replicated across multiple drives, servers, and even data centers, or split using erasure coding so lost pieces can be rebuilt from the rest. Combined with backups and monitoring, a single crashed server does not mean lost data.

**5. How is your confidence in navigating the Linux command line growing?**

My confidence is growing steadily. When the image failed to pull, I had to read the error messages carefully, work out that the problem was the registry and not my command, and try alternatives. Commands like `docker ps` and `docker logs` now feel like useful tools for checking what is happening instead of guesses. I am more comfortable typing commands and troubleshooting on my own.
