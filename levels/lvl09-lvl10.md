---
tags: [overthewire, bandit]
level: 9
---

# Bandit 9 → 10

**Challenge:** Password is in `data.txt`. It is one of the few readable strings, preceded by several `=` characters.

**Fix:** `strings data.txt | grep "=+"` — `strings` extracts readable text from binary junk, then grep finds the line with `=` signs.

> `strings` pulls out printable character sequences from any file. Super useful for binaries or garbled data.
