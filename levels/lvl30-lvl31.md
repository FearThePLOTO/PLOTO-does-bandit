---
tags: [overthewire, bandit]
level: 30
---

# Bandit 30 → 31

**Challenge:** Same repo setup, but the password is not in any branch or commit history. It's stored in a git tag.

**Fix:**
1. `git clone ssh://bandit30-git@localhost:2220/home/bandit30-git/repo`
2. `cd repo && git tag` — list all tags
3. `git show <tag-name>` — the tag message contains the password

> Tags are labels for specific commits. People use them for releases, but they can store secrets too. `git tag` + `git show` is the way to check.
