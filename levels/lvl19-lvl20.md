---
tags: [overthewire, bandit]
level: 19
---

# Bandit 19 → 20

**Challenge:** There is a setuid binary in home called `bandit20-do`. It runs commands as bandit20.

**Fix:** `bandit20-do cat /etc/bandit_pass/bandit20` — the binary executes whatever you pass as bandit20, so you can read the password file directly.

> Setuid binaries run with the file owner's permissions, not yours. This is how regular users can do root-level things safely — but if the binary is badly written, it's a privilege escalation vector.
