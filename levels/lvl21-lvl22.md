---
tags: [overthewire, bandit]
level: 21
---

# Bandit 21 → 22

**Challenge:** A cron job runs a script that writes the bandit22 password somewhere. Find it.

**Fix:**
1. `ls /etc/cron.d/` - find the cron job file
2. `cat /etc/cron.d/cronjob_bandit22` - see what script it runs
3. `cat /usr/bin/cronjob_bandit22.sh` - the script writes the password to a file in `/tmp`
4. `cat /tmp/<filename>` - there's your password

> Cron jobs are scheduled tasks. Always check `/etc/cron.d/`, `/etc/crontab`, and `/var/spool/cron/` when you need to find what's running automatically on a system.
