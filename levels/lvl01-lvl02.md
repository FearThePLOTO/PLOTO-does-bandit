---
tags:
  - overthewire
  - bandit
level: 1
---

# Bandit 1 -> 2

**Challenge:** File is named `-`. Running `cat -` freezes the terminal because `-` is interpreted as a flag.

**Fix:** `cat ./-` — the `./` prefix tells the shell it's a path, not a flag. Works for any file starting with `-`.

> The shell treats leading dashes as option indicators. Always prefix with `./` when dealing with files like this.
