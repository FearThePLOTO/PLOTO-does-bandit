---
tags: [overthewire, bandit]
level: 28
---

# Bandit 28 → 29

**Challenge:** Same repo setup as [[lvl27-lvl28]], but the password has been removed from the README. Find it in the git history.

**Fix:**
1. `git clone ssh://bandit28-git@localhost:2220/home/bandit28-git/repo`
2. `cd repo && cat README` - password is gone
3. `git log` - see the commit history, find the one that removed the password
4. `git checkout <commit-hash>` - to move to that commit
5. Or `git show <commit-hash>` - see the full diff for that commit
6. The removed line contains the password

> `git log` + `git diff` is how you audit what changed. Even if someone deletes a secret from the current code, it's still in the history unless they force-push to rewrite it.
