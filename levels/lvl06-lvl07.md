---
tags: [overthewire, bandit]
level: 6
---

# Bandit 6 → 7

**Challenge:** Find the password file anywhere on the server. It is owned by user bandit7, group bandit6, and is 33 bytes.

**Fix:** `find / -type f -user bandit7 -group bandit6 -size 33c` — same idea as [[lvl05-lvl06]], just different flags.

> `-user` and `-group` filter by ownership. Searching `/` instead of `.` means the whole filesystem. Might take a while.
