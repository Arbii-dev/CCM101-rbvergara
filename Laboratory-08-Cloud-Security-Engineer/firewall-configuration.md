# Firewall Configuration Documentation

## Commands Used to Secure the Server

1. **Allow SSH Access:**
   ```bash
   sudo ufw allow ssh
Description: This command permanently opens port 22 so that administrators can keep managing the server remotely without getting locked out.

2. **Set Default Deny Policy:**
 ```bash
  sudo ufw default deny incoming
  sudo ufw default allow outgoing
   ```
Description: These commands configure the foundational firewall rules to automatically block all incoming traffic by default while allowing all outgoing traffic.

3. **Allow Port 8080 (Web Application):**
 ```bash
   sudo ufw allow 8080/tcp 
   ```
Description: This command creates a specific rule to let legitimate web users access our Nginx application running on port 8080.

Important Security Note
What would happen if you ran sudo ufw enable before running sudo ufw allow ssh?
If you enabled the firewall first with a default deny policy, it would immediately block your current connection and lock you out of your own server.
