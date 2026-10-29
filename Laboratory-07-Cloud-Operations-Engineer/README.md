# Laboratory Activity 7:  The Cloud Operations Engineer

## Mission Overview
Congratulations! Your ability to deploy multi-tier architectures has proven your technical capabilities.
You have now been promoted to the Cloud Operations Team (often referred to in the industry as Site Reliability
Engineering, or SRE) at CloudNova Technologies.

Deploying a cloud application is only the first step; keeping it running smoothly is the real challenge.
When a server crashes or a web page takes ten seconds to load, you cannot simply guess what is wrong. You
must rely on Observability and Monitoring to see inside your infrastructure.

Using the KillerCoda Playground, you will step into the role of a Cloud Operations Engineer. You will
establish a performance baseline for your Linux server, deploy a containerized application, generate artificial web
traffic, and hunt down performance metrics and system logs to prove the application is healthy.
Remember: A developer hopes the application works; a Site Reliability Engineer uses metrics and logs to
prove it.

## Mission Objectives
- Utilize native Linux command-line tools to monitor host CPU, Memory, and Disk capacity.
- Deploy a web container and track its real-time performance using Docker metrics.
- Generate web traffic and extract application access logs for analysis.
- Translate raw performance data into a readable technical report using Markdown.
- Continue expanding a professional GitHub Cloud Computing Portfolio.

## Monitoring Commands Executed
During the course of this mission, the following terminal commands were utilized for system baseline checks, deployment, traffic simulation, and observability:

```bash
# 1. Host System Baseline Checks
free -h                  # Check memory (RAM) usage
df -h /                  # Check available root disk storage
top                      # View active running processes and CPU load

# 2. Container Deployment & Traffic Generation
docker run -d -p 8080:80 --name clientwebsite nginx   # Deploy Nginx web server
curl http://localhost:8080                            # Simulate standard user traffic
curl http://localhost:8080/hidden-admin-page          # Simulate a 404 error request

# 3. Observability & Monitoring
docker logs clientwebsite    # Retrieve container access and error logs
docker stats                 # View live streaming container resource consumption
```
## Skills Learned
* Host System Diagnostics: Acquired proficiency in using native Linux tools (free, df, top) to evaluate host server resource health and hardware baselines.

* Container Lifecycle Management: Successfully deployed and managed lightweight web server containers using Docker.

* Traffic Simulation & Log Analysis: Practiced generating test traffic with curl and inspecting container logs (docker logs) to isolate specific HTTP status codes (e.g., HTTP 200 vs. HTTP 404 errors).

* Real-Time Performance Tracking: Monitored live container resource utilization (CPU percentage, memory limits, and network I/O) using docker stats.

* Technical Documentation: Translated raw terminal outputs and performance metrics into structured, professional Markdown reports suitable for cloud engineering portfolios.

