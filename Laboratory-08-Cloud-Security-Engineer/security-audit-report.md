# Security Audit Report: Chapter 8 Core Concepts

## 1. The Principle of Least Privilege (PoLP)
The Principle of Least Privilege (PoLP) dictates that users, applications, and services should be granted only the minimal permissions strictly necessary to perform their required functions. This security model is critical for cloud environments; if an attacker compromises a single account, the blast radius is contained, preventing lateral movement and minimizing system-wide compromise.

## 2. Attack Surface
In the context of a virtual machine, the attack surface encompasses all exposed entry points, active network ports, and running services accessible for potential external exploitation. An increased number of open ports and active applications directly expands this surface, providing malicious actors with more opportunities to identify vulnerabilities and breach the server.

## 3. Default Deny Policy
A default deny policy is a foundational security posture where a firewall automatically drops all inbound traffic unless an explicit rule permits it. This approach is vastly superior to blacklisting individual malicious actors, as anticipating every potential threat IP address is impossible. By denying all traffic by default, any newly opened or overlooked port remains inherently secured until intentionally configured otherwise.
