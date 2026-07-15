---
tags: [overthewire, bandit]
level: 15
---

# Bandit 15 → 16

**Challenge:** Same as [[lvl14-lvl15]] but the service now uses SSL/TLS. Plain `nc` won't work.

**Fix:** `cat /etc/bandit_pass/bandit14 | openssl s_client -connect localhost:30001 -quiet`

> `openssl s_client` wraps the connection in SSL. The `-quiet` flag suppresses all the certificate debug noise. This is how you talk to encrypted services from the command line.
