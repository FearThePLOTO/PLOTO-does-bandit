---
tags: [overthewire, bandit]
level: 27
---

# Bandit 27 → 28

**Challenge:** There is a git repository at `ssh://bandit27-git@localhost:2220/home/bandit27-git/repo`. Clone it and find the password.

**Fix:** `git clone ssh://bandit27-git@bandit.labs.overthewire.org:2220/home/bandit27-git/repo` (password is same as bandit27) 

> Git repos can contain anything. Always check README, commit history, and branches for secrets. People accidentally commit passwords all the time.
