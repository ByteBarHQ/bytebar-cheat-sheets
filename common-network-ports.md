# Common Network Ports Cheat Sheet

> The 24 ports CompTIA Network+, Security+, and Cisco CCNA ask about most. Memorize the bold ones first.

## Must-Know Ports

| Port | Protocol | Service | Memory hook |
|---|---|---|---|
| **20/21** | TCP | FTP (data/control) | "FTP is 21, data rides 20" |
| **22** | TCP | SSH / SCP / SFTP | Secure remote — the secure 2's |
| **23** | TCP | Telnet | **Insecure** — never use, know why |
| **25** | TCP | SMTP | Sending email |
| **53** | TCP/UDP | DNS | UDP for lookups, TCP for zone transfers |
| **67/68** | UDP | DHCP (server/client) | "DHCP gives, 67/68 delivers" |
| **69** | UDP | TFTP | Trivial — no auth, PXE boot |
| **80** | TCP | HTTP | Unencrypted web |
| **110** | TCP | POP3 | Downloads email (deletes from server) |
| **123** | UDP | NTP | Time sync |
| **143** | TCP | IMAP | Email stays on server |
| **161/162** | UDP | SNMP (manager/trap) | Monitoring |
| **389** | TCP/UDP | LDAP | Directory lookups |
| **443** | TCP | HTTPS | Encrypted web |
| **445** | TCP | SMB/CIFS | Windows file sharing — ransomware loves it |
| **636** | TCP | LDAPS | LDAP over TLS |
| **993** | TCP | IMAPS | IMAP over TLS |
| **995** | TCP | POP3S | POP3 over TLS |
| **1433** | TCP | Microsoft SQL | Database default |
| **3306** | TCP | MySQL/MariaDB | Database default |
| **3389** | TCP | RDP | Windows remote desktop |
| **5432** | TCP | PostgreSQL | Database default |
| **5900** | TCP | VNC | Remote screen sharing |

## Secure vs Insecure Pairs (Security+ loves these)

| Insecure | Secure replacement |
|---|---|
| Telnet (23) | SSH (22) |
| FTP (21) | SFTP/SCP (22) or FTPS |
| HTTP (80) | HTTPS (443) |
| SNMP v1/v2 (161) | SNMP v3 (auth + encryption) |
| POP3 (110) / IMAP (143) | POP3S (995) / IMAPS (993) |

## Email Ports at a Glance

| Job | Plain | Secure |
|---|---|---|
| Send (SMTP) | 25 (587 submission) | 465 (SMTPS) |
| Receive/read | 110 POP3 / 143 IMAP | 995 / 993 |

---
📘 Full protocol deep-dives + practice questions: **[bytebarhq.com](https://bytebarhq.com)** — by [ByteBar](https://github.com/ByteBarHQ)
