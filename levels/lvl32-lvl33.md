---
tags: [overthewire, bandit]
level: 32
---

# Bandit 32 → 33

**Challenge:** You're dropped into an uppercase-only shell. All input is converted to uppercase, so normal commands don't work.

**Fix:** `$0` — this variable holds the path to the current shell. Since the shell itself is not affected by the uppercase filter, it executes normally and drops you into a real shell.

Then `cat /etc/bandit_pass/bandit33`.

> `$0` is a special variable — it's the name of the running script or shell. Since it bypasses the uppercase filter, it's your way out. This is a classic restricted shell escape.
