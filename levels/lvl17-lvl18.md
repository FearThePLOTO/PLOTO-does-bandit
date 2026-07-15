---
tags: [overthewire, bandit]
level: 17
---

# Bandit 17 → 18

**Challenge:** Two files in home: `passwords.old` and `passwords.new`. The password is the one line that changed between them.

**Fix:** `diff passwords.new passwords.old` - shows the differences. The line starting with `<` or `>` is your password.

> `diff` is the standard tool for comparing files. You'll use it constantly with git (`git diff`), config files, logs, anything.
