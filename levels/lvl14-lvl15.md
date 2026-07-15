---
tags: [overthewire, bandit]
level: 14
---

# Bandit 14 → 15

**Challenge:** Submit the current bandit14 password to port 30000 on localhost to get the next password.

**Fix:** `cat /etc/bandit_pass/bandit14 | nc localhost 30000` — pipe the password to netcat, which sends it to the service.

> `nc` (netcat) is the Swiss army knife of networking. Here it opens a TCP connection and sends your input. The service validates it and replies with the next password.
