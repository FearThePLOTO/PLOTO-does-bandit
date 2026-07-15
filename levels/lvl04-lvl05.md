---
tags:
  - overthewire
  - bandit
level: 4
---

# Bandit 4 → 5

**Challenge:** There are 9 files named `-file00` through `-file08` in `inhere/`. Only one is human-readable. The rest are binary garbage.

**Fix:** `file inhere/*` to check file types, then `cat` the one that says ASCII text.

> `file` is your friend when you need to know what something actually is. Don't waste time `cat`-ing binary files.
