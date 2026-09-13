# TCP vs UDP Cheat Sheet

> The head-to-head every Network+, Security+, and CCNA exam asks about.

## Side by Side

| | **TCP** | **UDP** |
|---|---|---|
| Full name | Transmission Control Protocol | User Datagram Protocol |
| Connection | Connection-oriented (handshake first) | Connectionless (fire and forget) |
| Reliability | Guaranteed delivery, ordered, error-checked | Best effort — no guarantees |
| Speed | Slower (overhead) | Faster (minimal overhead) |
| Header size | 20 bytes | 8 bytes |
| Use when | Accuracy matters | Speed matters |

## The Three-Way Handshake (TCP)

```
Client ──SYN──▶ Server
Client ◀─SYN/ACK── Server
Client ──ACK──▶ Server
```

**Teardown:** FIN / FIN-ACK / ACK

## Use TCP When…

- Web browsing (HTTP/HTTPS)
- Email (SMTP, IMAP, POP3)
- File transfer (FTP, SFTP)
- Remote admin (SSH, RDP)

## Use UDP When…

- DNS lookups (port 53)
- DHCP (ports 67/68)
- Streaming / VoIP / gaming (speed > perfection)
- NTP time sync (123), SNMP (161), TFTP (69)

## Exam Traps

- **"Which is connectionless?"** → UDP
- **SYN flood attack** → abuses the TCP handshake (half-open connections)
- **TCP uses sequencing + acknowledgments**; UDP has neither
- DNS uses **UDP** for queries but **TCP** for zone transfers

---
📘 Full protocol deep-dives + practice questions: **[bytebarhq.com](https://bytebarhq.com)** — by [ByteBar](https://github.com/ByteBarHQ)
