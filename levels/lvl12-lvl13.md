---
tags: [overthewire, bandit]
level: 12
---

# Bandit 12 → 13

**Challenge:** `data.txt` is a hex dump of a file that has been compressed multiple times. You need to peel back each layer to get the password.

**Step by step:**

1. `xxd -r data.txt compressed` — convert hex dump back to binary
2. `file compressed` — check what it is (gzip)
3. Rename to `.gz` and decompress: `mv compressed data.gz && gzip -d data.gz`
4. Repeat: check with `file`, rename to correct extension, decompress. It goes gzip → tar → tar → bzip2 → gzip → plaintext

**The loop looks like this:**
```
file <filename>        # identify it
mv <filename> <name>.<ext>   # rename to correct extension
<tool> -d <name>.<ext>       # decompress/extract
```

> The key insight: `file` tells you what each layer is. Don't guess — check, then decompress. This level is tedious but the pattern is always the same.
