# Day-12-Automation
---
##### Cron:
 - Cron is a time-based job scheduler in Unix-like operating systems.
 - It allows users to automatically run scripts, commands, or programs at specified times and dates.
##### Cron Works:
###### Cron Daemon:
 - The cron service (crond) runs in the background and constantly checks the configuration files for scheduled tasks.
###### Crontab Files:
 - Users define their scheduled tasks in a file called crontab. Each line in a crontab file represents a job, specifying when and what to execute.
```
0 5 * * * /home/user/backup.sh
```
- This will run the backup.sh script every day at 5:00 AM.
---
##### User Cron Jobs:
 - For personal automation, managed by individual users.
 - Each user has a personal crontab file, managed via the crontab -e command.
 - Jobs run with the privileges of the user who created them.
```
0 8 * * * /home/username/myscript.py
```
 - A user sets up a cron job to run a Python script every day at 8 AM

##### System cron jobs:
 - For system wide tasks, managed by root or admin.
 - System-wide cron jobs are defined in
   (/etc/crontab )(/etc/cron.d/)
   (/etc/cron.daily/, /etc/cron.hourly/, /etc/cron.weekly/, /etc/cron.monthly/)
 - Used for system maintenance tasks like log rotation, updates, backups, and monitoring.
```
0 2 * * * root /usr/bin/cleanup.sh
```
 - A job in /etc/crontab to clean temp files every night.
---
##### VM State:
 - VM (Virtual Memory) State refers to the current status of memory usage and swapping on a Linux/Unix system.
 - Key Metrics - Free memory, Used memory, Swap usage, Cache/buffer usage.
```
vmstat 2 5
```
 - This displays system memory, processes, paging, block IO, traps, and CPU activity.
---
##### iostat:
 - iostat (Input/Output Statistics) is a Linux/Unix command-line tool to monitor system input/output device loading by observing the time devices are active in relation to their average transfer rates.
```
iostat
iostat 2
```
 - This Command To get updated statistics every 2 seconds.
##### Firewall:
 - A firewall acts as a barrier between trusted and untrusted networks,
helping to keep your systems safe from cyber threats and unauthorized access.
---
#### Task:
###### Verify Scheduled Jobs:
```
crontab -l
```
 - It's Check all cron jobs for the current User.
```
crontab -e
```
 - This will open your cron editor so you can add or modify scheduled tasks.
 - Choose The editor and Add your Scheduled tasks.
```
0 2 * * * /usr/local/bin/daily_backup.sh >> /var/log/daily_backup.log 2>&1
```
- Daily backup at 2 AM.
```
0 3 * * 0 /usr/local/bin/cleanup.sh >> /var/log/cleanup.log 2>&1
```
 - Weekly cleanup on Sunday at 3 AM.
---



















---

 
