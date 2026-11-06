# Laboratory 9: The Cloud Automation Engineer

## Mission Overview
Stepping into the role of a Cloud Automation Engineer at CloudNova Technologies, this laboratory focuses on eliminating manual administrative tasks by writing Bash automation scripts, managing file permissions, and scheduling automated backups using the Linux cron utility.

## Objectives
- Understand fundamental Bash shell script syntax, including variables and basic commands.
- Use the nano command-line text editor to write and save executable scripts.
- Modify Linux file permissions using the `chmod` command.
- Understand task scheduling and the syntax of a Linux crontab.
- Document automation code and Cron job configurations using Markdown.
## Commands Executed
- `mkdir app-data` - Establishes a mock directory simulating production client files.
- `echo "This is critical client data." > app-data/data.txt` - Populates a sample text file for testing.
- `nano backup.sh` - Launches the command-line editor to draft the backup routine.
- `chmod +x backup.sh` - Updates the script's access controls to permit direct execution.
- `./backup.sh` - Runs the custom automation script manually for testing.
- `ls -l backups/` - Confirms that the target `.tar.gz` archive was successfully created.
- `crontab -l` - Displays currently active automated cron task schedules.
- `env EDITOR=nano crontab -e` - Opens the system cron table configuration interface.

## Skills Learned
- Core shell scripting principles and dynamic variable management.
- Linux file access control administration via `chmod`.
- Automated directory archiving and compression utilizing `tar`.
- Task scheduling implementation and cron schedule syntax.
