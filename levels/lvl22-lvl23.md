---
tags: [overthewire, bandit]
level: 22
---

# Bandit 22 → 23

**Challenge:** A cron job runs a script that copies bandit23's password to `/tmp`. You need to figure out the filename.

**The script (`/usr/bin/cronjob_bandit23.sh`):**
```bash
myname=$(whoami)
mytarget=$(echo I am user $myname | md5sum | cut -d ' ' -f 1)
cat /etc/bandit_pass/$myname > /tmp/$mytarget
```

It runs as bandit23, so it copies bandit23's password to a file named after the MD5 of `I am user bandit23`.

**Fix:**
1. `echo I am user bandit23 | md5sum | cut -d ' ' -f 1` - generates the filename
2. `cat /tmp/<hash>` - read the password

> Read the script carefully. `whoami` returns bandit23 when cron runs it, not you. The filename is predictable because it's based on a fixed string.
