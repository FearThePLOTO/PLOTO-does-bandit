---
tags: [overthewire, bandit]
level: 10
---

# Bandit 10 → 11

**Challenge:** Password is in `data.txt`, which is base64 encoded.

**Fix:** `base64 -d data.txt` — decodes base64 back to plaintext.

> Base64 is encoding, not encryption. It's reversible with a single command. You'll see it everywhere in URLs, emails, APIs.
