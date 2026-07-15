---
tags:
  - overthewire
  - bandit
level: 5
---

# Bandit 5 → 6

**Challenge:** Find the password file inside `inhere/`. It's human-readable, exactly 1033 bytes, and not executable.

**Fix:** `find . -type f ! -executable -size 1033c` - chain conditions with `find` to narrow down fast.

> `find` flags: `-type f` (files only), `! -executable` (not a binary), `-size 1033c` (exact byte size). Learn `find` early, it saves so much time.
