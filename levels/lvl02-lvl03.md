---
tags:
  - overthewire
  - bandit
level: 2
---

# Bandit 2 -> 3

**Challenge:** File is named `--spaces in this file--`. Same deal as [[lvl01-lvl02]], but now with spaces.

**Fix:** `cat './--spaces in this file--'` — wrap the whole path in quotes to handle the spaces.

> Spaces in filenames are always a pain. Quote them or escape with `\`. Applies everywhere, not just Bandit.
