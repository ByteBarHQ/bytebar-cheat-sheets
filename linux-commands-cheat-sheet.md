# Linux Commands Cheat Sheet

> The 40+ commands CompTIA Linux+, Security+, and every sysadmin interview expect.

## Navigation & Files

| Command | Does what |
|---|---|
| `pwd` | Print working directory |
| `ls -la` | List all files incl. hidden, with details |
| `cd -` | Jump back to previous directory |
| `cp -r src dst` | Copy recursively |
| `mv old new` | Move / rename |
| `rm -rf dir` | Delete recursively, no prompt (⚠️ careful) |
| `mkdir -p a/b/c` | Create nested directories |
| `touch file` | Create empty file / update timestamp |
| `find / -name "*.log"` | Search by name |
| `grep -r "error" /var/log` | Search inside files, recursive |
| `cat / less / head / tail` | View files (`tail -f` follows live) |

## Permissions

| Command | Does what |
|---|---|
| `ls -l` | Show permissions (`-rwxr-xr--`) |
| `chmod 755 file` | rwx / r-x / r-x — standard for scripts |
| `chmod 644 file` | rw- / r-- / r-- — standard for files |
| `chown user:group file` | Change owner |
| `sudo !!` | Re-run last command as root |

**Numeric recap:** 4 = read, 2 = write, 1 = execute → 7 = rwx, 6 = rw-, 5 = r-x, 4 = r--

## Networking

| Command | Does what |
|---|---|
| `ip a` | Show interfaces + IPs (modern `ifconfig`) |
| `ip r` | Show routing table |
| `ping -c 4 host` | Test connectivity |
| `ss -tulpn` | Listening ports + processes (modern `netstat`) |
| `curl -I https://site` | Fetch headers |
| `dig +short example.com` | DNS lookup |
| `traceroute host` | Path packets take |
| `ssh user@host` | Secure remote shell |
| `scp file user@host:/path` | Secure copy |

## System & Processes

| Command | Does what |
|---|---|
| `ps aux \| grep nginx` | Find processes |
| `top` / `htop` | Live process monitor |
| `kill -9 PID` | Force-kill a process |
| `systemctl status nginx` | Service status |
| `systemctl restart nginx` | Restart a service |
| `journalctl -u nginx -f` | Follow service logs |
| `df -h` | Disk space (human-readable) |
| `du -sh *` | Directory sizes |
| `free -h` | Memory usage |
| `uptime` | Load + uptime |
| `uname -a` | Kernel / system info |

## Text Power Tools

| Command | Does what |
|---|---|
| `grep -i "fail" log` | Case-insensitive search |
| `sort file \| uniq -c` | Count unique lines |
| `awk '{print $1}' file` | Print column 1 |
| `sed 's/old/new/g' file` | Find and replace |
| `wc -l file` | Count lines |
| `history \| grep ssh` | Search command history |

---
📘 Full Linux + command-line study guides: **[bytebarhq.com](https://bytebarhq.com)** — by [ByteBar](https://github.com/ByteBarHQ)
