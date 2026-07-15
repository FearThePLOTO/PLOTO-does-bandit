---
tags:
  - overthewire
  - bandit
level: 3
---

# Bandit 3 -> 4

**Challenge:** Password is in a hidden file (starts with `.`).

**Fix:** `ls -a` to see hidden files, then `cat <filename>`.

> Hidden files are just files prefixed with `.`. They don't show up in plain `ls`. This is standard Unix behavior, not a trick.
