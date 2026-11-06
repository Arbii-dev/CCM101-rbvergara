# Backup Script Technical Documentation

## Script Source Code

#!/bin/bash
# Automated Backup Script for CloudNova Technologies
SOURCE_DIR="app-data"
BACKUP_DIR="backups"
TIMESTAMP=$(date +"%Y%m%d_%H%M%S")
echo "Initiating automated backup..."
# Create the backup directory if it does not exist
mkdir -p $BACKUP_DIR
# Compress the source directory into a tarball (.tar.gz)
tar -czf $BACKUP_DIR/backup_$TIMESTAMP.tar.gz $SOURCE_DIR
echo "Backup completed successfully at $TIMESTAMP!"


Understanding chmod +x

By default, Linux blocks newly created text files from running as executable programs for security reasons. Running the chmod +x backup.sh command modifies the file permissions by adding execution rights, enabling the operating system to run the file directly as an executable script.

Cron Expression Breakdown

The cron expression used to schedule the automated backup is:
0 2 * * * /root/backup.sh

0 (Minute): Runs on the 0th minute of the hour.

2 (Hour): Runs during the 2nd hour of the day (2:00 AM).

* (Day of Month): Runs on every day of the month.

* (Month): Runs during every month of the year.

* (Day of Week): Runs on every day of the week.
