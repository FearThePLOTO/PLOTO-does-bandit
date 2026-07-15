---
tags: [overthewire, bandit]
level: 25
---

# Bandit 25 → 26

**Challenge:** Bandit26's shell is not `/bin/bash`. You get an SSH key from bandit25, but logging in drops you into a restricted shell that exits immediately.

**Fix:**
1. `cat /etc/passwd | grep bandit26` — see what shell it uses (it's `more`)
2. resize the terminal in your machine to have a small longitude for a brief time before the logout happens
3. Log in with the key: `ssh -i bandit26.sshkey bandit26@localhost -p 2220`
4. The `more` pager starts and shows text. Press `v` to open in `vi`
5. In `vi`, type `:set shell=/bin/bash` to change the default shell then `:shell`. 
6. `cat /etc/bandit_pass/bandit26`

> When you land in a restricted shell, look for ways to escape. `more` and `less` let you open an editor, and editors let you run shell commands. The chain is always: restricted shell → editor → real shell.
