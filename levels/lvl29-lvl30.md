---
tags: [overthewire, bandit]
level: 29
---

# Bandit 29 → 30

**Challenge:** Same repo setup, but the password is not in the main branch or its history. It's on a different branch.

**Fix:**
1. `git clone ssh://bandit29-git@localhost:2220/home/bandit29-git/repo`
2. `cd repo && git branch -a` - list all branches, including remote ones
3. or `git log --all` to see all the Log files for the all the branches
4. `git checkout <branch-name>` - switch to the other branch
5. `cat README` - password is in there

> `git branch -a` shows local and remote branches. People often push secrets to a dev branch and forget about it. Always check all branches when auditing a repo.
> `git log --all` shows all the log for all the branches. People often leave some hints that indicate that they have made something wrong.
