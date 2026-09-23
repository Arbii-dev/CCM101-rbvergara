# Laboratory 04: Reflection

There can be a big difference between containers and virtual machines. First, boot time and setup process is faster using containers than installing an operating system on traditional VMs. While VM requires provisioning hardware, partitioning virtual disk and booting an entire OS kernel, containers simply spawns a process which boots in mere seconds by sharing the host kernel.

Port mapping (`-p 8080:80`) is crucial when running a web server inside a container because containers operate within an isolated network namespace. Without explicit port forwarding, traffic cannot reach the container's internal web service; mapping host port 8080 to container port 80 acts as a secure bridge, allowing external clients or local tools like `curl` to access the application. 

When you delete a container with the docker rm command, all the data saved inside it disappears. This shows that containers are temporary, which is why we use external volumes or storage folders to keep important data safe.

Containers help developers and IT teams work together better by packaging the code and everything it needs into a single box. This stops the common problem where code works on a developer's computer but breaks on the server, making sure it runs the exact same way everywhere.

Doing this lab makes my GitHub portfolio much stronger. It shows I have real, hands-on skills with cloud technology and container management, which is a great step forward in learning practical skills for my IT career.
