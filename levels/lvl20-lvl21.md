---
tags: [overthewire, bandit]
level: 20
---

# Bandit 20 → 21

**Challenge:** A setuid binary in home connects to a port you specify as an argument. It reads a line, compares it to bandit20's password. If correct, it gives you bandit21's password.

**Fix:**
1. Start a listener that sends the password: `echo "$(cat /etc/bandit_pass/bandit20)" | nc -l -p <port>` or `nc -l <port> < /etc/bandit_pass/bandit20`
2. In another session, run the binary: `./suconnect <port>`
3. The binary reads your password, validates it, and prints the next one.

> Use `&`, `tmux`, or `screen` to run the listener and the binary at the same time. The binary expects the password on a port — you need something listening there first.
