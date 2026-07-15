---
tags: [overthewire, bandit]
level: 18
---

# Bandit 18 → 19

**Challenge:** Password is in `readme` in home, but `.bashrc` has been modified to kick you out immediately on login.

**Fix:** `ssh bandit.labs.overthewire.org -p 2220 -l bandit18 -t 'cat readme'` - the `-t` flag forces a pseudo-terminal and runs the command before `.bashrc` can log you out.

> `-t` is useful when you need to execute something on a remote shell without going through the normal login sequence. It allocates a terminal even for single commands.
