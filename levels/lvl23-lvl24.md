---
tags: [overthewire, bandit]
level: 23
---

# Bandit 23 → 24

**Challenge:** A cron job runs every script in `/var/spool/bandit24/foo/`, then deletes it. Your script must run as bandit24 to read bandit24's password.

**Fix:**
1. `mktemp -d` - create a temp directory
2. Write a script there:
```bash
#!/bin/bash
mkdir -p /tmp/yourtempdir/$(cat /etc/bandit_pass/bandit24)
```
3. Make it executable and world-readable: `chmod +rx script.sh`
4. Make your temp dir accessible: `chmod 777 /tmp/yourtempdir`
5. `cp script.sh /var/spool/bandit24/foo/`
6. Wait a few seconds, then `ls -la`

> The cron job runs your script as bandit24, then deletes it. You can't read the password file directly, but your script can write it somewhere you can access. Permissions matter - the temp dir and script both need to be accessible by bandit24.
