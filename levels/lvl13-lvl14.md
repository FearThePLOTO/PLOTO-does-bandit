---
tags: [overthewire, bandit]
level: 13
---

# Bandit 13 → 14

**Challenge:** Password is stored in `/etc/bandit_pass/bandit14`, but you can only read it as bandit14. You are given an SSH private key for bandit14.

**Method 1 - Copy the key to your machine:**
1. `cat sshkey.private` and copy the contents
2. On your local machine, paste it into a file: `vim bandit14_key`
3. Fix permissions: `chmod 600 bandit14_key`
4. Connect: `ssh -i bandit14_key bandit14@bandit.labs.overthewire.org -p 2220`
5. `cat /etc/bandit_pass/bandit14`

**Method 2 - SCP the key:**
1. `scp -P 2220 sshkey.private bandit13@bandit.labs.overthewire.org:/tmp/` (from your machine)
2. SSH into bandit13, then from there: `scp -P 2220 sshkey.private bandit14@bandit.labs.overthewire.org:/tmp/`
3. SSH as bandit14 using the key

> SSH keys are just text. Copy-paste works fine. The `chmod 600` is required - SSH refuses to use keys with open permissions.
