# Laboratory 2: Build the Cloud Infrastructure Blueprint

## Mission Overview
Congratulations

Your onboarding has been successfully completed, and your Cloud Computing Portfolio has been approved by
your supervisor.

CloudNova Technologies has now assigned you to your first official project.

Before deploying cloud services, every cloud engineer must understand the infrastructure that powers modern
cloud computing. Your mission is to investigate the components of cloud infrastructure, identify how compute,
storage, networking, and identity services work together, and document your findings as if you were preparing
technical documentation for a client.

Using the KillerCoda Playground, Linux tools, official cloud documentation, and your GitHub Cloud Computing
Portfolio, you will complete a series of engineering tasks that simulate the planning phase of a cloud deployment.
Remember: Great cloud engineers build systems—but exceptional cloud engineers document and justify
every design decision.

---

## Objectives
### At the end of this laboratory activity, you should be able to: 

* Explain the major components of cloud infrastructure.
* Investigate the hardware and software resources available in a Linux environment.
* Differentiate compute, storage, networking, and identity resources.
* Interpret the relationship between cloud infrastructure components.
* Create professional technical documentation using Markdown.
* Continue building a structured GitHub Cloud Computing Portfolio. 


---

## Cloud Infrastructure Components

* **Compute Resources:** Processing power and volatile memory (vCPUs and RAM) used to execute workloads.
* **Storage Resources:** Persistent block storage volumes (`ext4` disks), specialized boot partitions, and ephemeral memory-backed temporary storage (`tmpfs`).
* **Networking Resources:** Virtual interfaces, IP addressing schemes (`enp1s0`, `lo`), and container bridges (`docker0`) that route traffic securely.
* **Operating System:** The foundational software layer (Ubuntu 24.04.4 LTS / Linux kernel) that manages hardware and isolates user-space processes.

---

## Tools Used
* KillerCoda, Github, Markdown, Draw.io

---

## Linux Commands Executed
* `cat /etc/os-release` – Displays operating system release and version details.
* `uname -r` / `uname` – Reports the active Linux kernel architecture and version.
* `lscpu` – Outlines CPU architecture, vendor ID, model name, and core configurations.
* `free` – Shows total, used, and available physical RAM and swap allocation.
* `df` / `df -Th` – Displays mounted filesystems, total disk capacity, and file type formats.
* `hostname` – Prints the network hostname assigned to the machine.
* `ip -4 addr show` – Lists active IPv4 network interfaces and assigned addresses.

---

## Skills Learned
* Inspecting hardware and software data in a Linux operating system via the command line.
* Physically understanding abstract cloud computing components (Compute, Storage, Networking).
* Understanding and visualizing cloud infrastructure via making thy own diagram.
* Comparing and contrasting services across major public cloud providers (AWS, Azure, and GCP).

---

## Challenges Encountered
* Minor syntax changes or missing command flags (such as differentiating between `uname -r` and `uname`) during initial system exploration.
* Understanding and differentiating the three common cloud service providers without being lost in miniscule features and focusing on integral information
