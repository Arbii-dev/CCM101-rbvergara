# Laboratory 8: The Cloud Security Engineer

## Mission Overview
During this exercise, we assumed the position of a Cloud Security Engineer for CloudNova Technologies. Our primary goal was to fortify a freshly provisioned, vulnerable Ubuntu server by applying a defense-in-depth framework via a host-based firewall (UFW).

## Objectives
- Analyze the server's attack surface and master the Principle of Least Privilege (PoLP).
- Conduct a foundational security audit examining active listening ports on the Linux machine.
- Set up the Uncomplicated Firewall (UFW) enforcing a strict Default Deny posture.
- Apply precise port management rules to selectively permit SSH and HTTP/8080 connections.
- Record all firewall configurations and security guidelines in Markdown format.
- Refresh and update the official GitHub Cloud Computing Portfolio.

## Commands Executed
- `docker run -d --name secure-web-app -p 8080:80 nginx` - Provisioned the test Nginx web container in detached mode.
- `sudo ufw allow ssh` - Whitelisted incoming SSH connections on port 22.
- `sudo ufw default deny incoming` - Established a baseline security policy rejecting all inbound requests.
- `sudo ufw default allow outgoing` - Configured outbound rules to permit all traffic leaving the server.
- `sudo ufw enable` - Turned on the UFW firewall service.
- `sudo ufw status verbose` - Inspected the comprehensive, verbose status of active firewall rules.
- `sudo ufw allow 8080/tcp` - Permitted explicit TCP traffic over port 8080.
- `sudo ufw status numbered` - Displayed the index-numbered rule list for straightforward verification.

## Skills Learned
- Executing server hardening practices and network defense configurations.
- Administering host-level firewalls utilizing UFW within an Ubuntu environment.
- Enforcing Default Deny postures alongside fine-grained port restrictions.
- Crafting technical documentation and maintaining evidence-driven project portfolios.
