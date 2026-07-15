---
tags: [overthewire, bandit]
level: 7
---

# Bandit 7 → 8

**Challenge:** Password is in `data.txt`, on the same line as the word `millionth`.

**Fix:** `grep "millionth" data.txt` — grep searches for the pattern and prints the matching line.

> `grep` is one of the most used tools in Linux. Pipe it, redirect it, chain it. Learn it well.
