```
┌──(bandit@labs)-[~]
└─$ ssh bandit0@bandit.labs.overthewire.org -p 2220
     _                     _ _ _   
    | |__   __ _ _ __   __| (_) |_ 
    | '_ \ / _` | '_ \ / _` | | __|
    | |_) | (_| | | | | (_| | | |_ 
    |_.__/ \__,_|_| |_|\__,_|_|\__|

    [+] 33 levels · recon · Wargame for beginners
```

> [!NOTE]
> **OverTheWire: Bandit** is a beginner wargame that teaches the basics of remote server access, Linux commands, and security thinking. You SSH into a server and solve levels by finding passwords hidden in tricky ways.
>
> [Official Site](https://overthewire.org/wargames/bandit/)

---

## Levels 00 - 10 · The Basics

| # | Level | Key Concept |
|---|-------|-------------|
| 0 | [lvl00-lvl01](levels/lvl00-lvl01.md) | SSH login, `ls`, `cat` |
| 1 | [lvl01-lvl02](levels/lvl01-lvl02.md) | Files starting with `-` need `./` prefix |
| 2 | [lvl02-lvl03](levels/lvl02-lvl03.md) | Files with spaces need quoting |
| 3 | [lvl03-lvl04](levels/lvl03-lvl04.md) | Hidden files — `ls -a` |
| 4 | [lvl04-lvl05](levels/lvl04-lvl05.md) | `file` to identify file types |
| 5 | [lvl05-lvl06](levels/lvl05-lvl06.md) | `find` with size/type filters |
| 6 | [lvl06-lvl07](levels/lvl06-lvl07.md) | `find` with user/group ownership |
| 7 | [lvl07-lvl08](levels/lvl07-lvl08.md) | `grep` to search file contents |
| 8 | [lvl08-lvl09](levels/lvl08-lvl09.md) | `sort` + `uniq` for unique lines |
| 9 | [lvl09-lvl10](levels/lvl09-lvl10.md) | `strings` on binary files |
| 10 | [lvl10-lvl11](levels/lvl10-lvl11.md) | `base64 -d` decoding |

## Levels 11 - 20 · Encoding & Permissions

| # | Level | Key Concept |
|---|-------|-------------|
| 11 | [lvl11-lvl12](levels/lvl11-lvl12.md) | `tr` for ROT13 rotation |
| 12 | [lvl12-lvl13](levels/lvl12-lvl13.md) | Multi-layer decompression (`xxd`, `gzip`, `bzip2`, `tar`) |
| 13 | [lvl13-lvl14](levels/lvl13-lvl14.md) | SSH key authentication |
| 14 | [lvl14-lvl15](levels/lvl14-lvl15.md) | `nc` — netcat for network services |
| 15 | [lvl15-lvl16](levels/lvl15-lvl16.md) | `openssl s_client` for SSL/TLS |
| 16 | [lvl16-lvl17](levels/lvl16-lvl17.md) | Port scanning 31000-32000 |
| 17 | [lvl17-lvl18](levels/lvl17-lvl18.md) | `diff` to compare files |
| 18 | [lvl18-lvl19](levels/lvl18-lvl19.md) | SSH `-t` to bypass `.bashrc` |
| 19 | [lvl19-lvl20](levels/lvl19-lvl20.md) | Setuid binaries |
| 20 | [lvl20-lvl21](levels/lvl20-lvl21.md) | Setuid + netcat over port |

## Levels 21 - 33 · Cron, Git & Escapes

| # | Level | Key Concept |
|---|-------|-------------|
| 21 | [lvl21-lvl22](levels/lvl21-lvl22.md) | Cron jobs — `/etc/cron.d/` |
| 22 | [lvl22-lvl23](levels/lvl22-lvl23.md) | Cron + MD5 hash prediction |
| 23 | [lvl23-lvl24](levels/lvl23-lvl24.md) | Drop scripts in cron directories |
| 24 | [lvl24-lvl25](levels/lvl24-lvl25.md) | Brute-force with bash loop |
| 25 | [lvl25-lvl26](levels/lvl25-lvl26.md) | Escape restricted shell (`more` → `vi` → `sh`) |
| 26 | [lvl26-lvl27](levels/lvl26-lvl27.md) | Setuid binary (repeat) |
| 27 | [lvl27-lvl28](levels/lvl27-lvl28.md) | `git clone` — basic repo |
| 28 | [lvl28-lvl29](levels/lvl28-lvl29.md) | `git log` + `git diff` — history |
| 29 | [lvl29-lvl30](levels/lvl29-lvl30.md) | `git branch -a` — branches |
| 30 | [lvl30-lvl31](levels/lvl30-lvl31.md) | `git tag` + `git show` — tags |
| 31 | [lvl31-lvl32](levels/lvl31-lvl32.md) | `git push` — server hooks |
| 32 | [lvl32-lvl33](levels/lvl32-lvl33.md) | Escape uppercase shell with `$0` |

---
