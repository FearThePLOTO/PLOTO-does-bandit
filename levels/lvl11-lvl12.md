---
tags: [overthewire, bandit]
level: 11
---

# Bandit 11 → 12

**Challenge:** Password is in `data.txt`. Every letter has been rotated by 13 positions (ROT13).

**Fix:** `tr 'A-Za-z' 'N-ZAn-za' < data.txt` — shifts each letter 13 spots. A becomes N, B becomes O, etc.

> ROT13 is a toy cipher. It's symmetric — running it twice gives you the original text. Used mostly for spoilers, not security.
