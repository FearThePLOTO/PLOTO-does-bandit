---
tags: [overthewire, bandit]
level: 16
---

# Bandit 16 → 17

**Challenge:** Submit the bandit16 password to a port between 31000 and 32000 on localhost. But first you need to figure out which port is the right one - some speak SSL, some don't, and only one gives you the password.

**Step 1 - Find open ports:**
`nmap -p 31000-32000 localhost` - shows which ports are listening.

**Step 2 - Figure out which speaks SSL:**
Try connecting to each open port. Non-SSL ports echo back whatever you send. The SSL port needs `openssl s_client`.

**Step 3 - Send the password:**
`cat /etc/bandit_pass/bandit16 | openssl s_client -connect localhost:<port> -quiet`, and you will get a private SSH key for the next lvl.

> If you get "DONE" or "RENEGOTIATING", check the manpage for `s_client` - the `-quiet` flag handles most of it. The trick is distinguishing the real server from the echo servers.
