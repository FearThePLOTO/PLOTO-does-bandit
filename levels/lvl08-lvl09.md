---
tags: [overthewire, bandit]
level: 8
---

# Bandit 8 → 9

**Challenge:** Password is the only line in `data.txt` that appears exactly once. Every other line is duplicated.

**Fix:** `sort data.txt | uniq -u` — sort first, then `uniq -u` prints only unique lines.

> `uniq` only works on adjacent duplicate lines, which is why you need `sort` first. Classic combo.
