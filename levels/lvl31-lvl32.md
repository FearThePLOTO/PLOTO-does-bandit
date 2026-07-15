---
tags: [overthewire, bandit]
level: 31
---

# Bandit 31 → 32

**Challenge:** Clone the repo, read the README. It tells you to push a file with specific content to trigger the password.

**Fix:**
1. `git clone ssh://bandit31-git@localhost:2220/home/bandit31-git/repo`
2. `cd repo && cat README` — tells you to push a file named `key.txt` with content `May I come in?`
3. `echo "May I come in?" > key.txt`
4. `git add key.txt && git commit -m "add key"`
5. `git push` — the server receives the push and replies with the password

> This is the first time you're writing to a git repo instead of just reading. The server-side hook reads your push and sends back the password. Git hooks can run arbitrary code on push — that's how this works.
