# Checkpoint 7 - Mission Reflection

Stepping into the shoes of a Cloud Operations Engineer really opened my eyes to the fact that getting a cloud application up and running is only half the battle; keeping it stable is where the real work begins. Working through this mission gave me a much deeper appreciation for infrastructure management and structured troubleshooting.

First off, checking the host server's core resources using commands like `free -h`, `top`, and `df -h /` is a must, even if every container looks completely healthy on the surface. Containers rely entirely on the underlying host hardware—if the host runs out of disk space because of bloated logs or starves for memory, it will drag down everything running on it regardless of how well-behaved the individual containers are.

Second, when a user reaches out saying they can't log in or something's broken, running `docker logs` is basically checking security camera footage. It gives you an exact timestamped history of incoming requests and error codes, letting you pinpoint whether the issue is a bad user input or a crashed backend service without having to guess.

Third, there's a big operational difference between logs and metrics. Logs give you the historical narrative and text-based event details of what happened, whereas metrics give you a live, numerical pulse of resource usage like instantaneous CPU percentages and memory consumption.

Fourth, to handle thousands of containers at once, massive enterprises rely heavily on automation stacks like Prometheus to pull time-series data and Grafana to visualize everything on centralized dashboards. 

Looking back, hands-on practice with these tools has vastly improved my confidence in diagnosing Linux systems methodically instead of stumbling through guesswork.
