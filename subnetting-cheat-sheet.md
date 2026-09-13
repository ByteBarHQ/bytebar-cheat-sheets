# Subnetting Cheat Sheet

> The 30-second subnetting trick, CIDR tables, and everything CompTIA and Cisco expect you to know cold.

## The Subnetting Trick (do this on every question)

Given an IP and CIDR (e.g. `192.168.1.77/26`):

1. **Block size** = 256 − interesting octet value → 256 − 192 = **64**
2. **Subnets** fall on multiples of the block size → 0, 64, 128, 192
3. **77** falls between 64 and 128 → subnet is **192.168.1.64**
4. **Range:** 192.168.1.64 – 192.168.1.127 · **Broadcast:** .127 · **Usable:** .65 – .126

## CIDR Quick Table

| CIDR | Subnet Mask | Wildcard | Usable Hosts |
|---|---|---|---|
| /24 | 255.255.255.0 | 0.0.0.255 | 254 |
| /25 | 255.255.255.128 | 0.0.0.127 | 126 |
| /26 | 255.255.255.192 | 0.0.0.63 | 62 |
| /27 | 255.255.255.224 | 0.0.0.31 | 30 |
| /28 | 255.255.255.240 | 0.0.0.15 | 14 |
| /29 | 255.255.255.248 | 0.0.0.7 | 6 |
| /30 | 255.255.255.252 | 0.0.0.3 | 2 |
| /23 | 255.255.254.0 | 0.0.1.255 | 510 |
| /22 | 255.255.252.0 | 0.0.3.255 | 1,022 |
| /21 | 255.255.248.0 | 0.0.7.255 | 2,046 |
| /16 | 255.255.0.0 | 0.0.255.255 | 65,534 |

**Formula:** usable hosts = 2^(host bits) − 2 (subtract network + broadcast)

## Private IP Ranges (RFC 1918)

| Class | Range | CIDR | Addresses |
|---|---|---|---|
| A | 10.0.0.0 – 10.255.255.255 | /8 | 16,777,216 |
| B | 172.16.0.0 – 172.31.255.255 | /12 | 1,048,576 |
| C | 192.168.0.0 – 192.168.255.255 | /16 | 65,536 |

Also know: **127.0.0.0/8** = loopback · **169.254.0.0/16** = APIPA (link-local, DHCP failed)

## Classful Boundaries

| Class | First Octet | Default Mask |
|---|---|---|
| A | 1 – 126 | /8 |
| B | 128 – 191 | /16 |
| C | 192 – 223 | /24 |

(127 is reserved — loopback, not Class A usable.)

## Special-Purpose Addresses

| Address | Meaning |
|---|---|
| 0.0.0.0/0 | Default route — "everything" |
| 255.255.255.255 | Limited broadcast — "everyone here" |
| Network address | First address in subnet (not assignable) |
| Broadcast address | Last address in subnet (not assignable) |

---
📘 Full subnetting walkthroughs + practice questions: **[bytebarhq.com](https://bytebarhq.com)** — by [ByteBar](https://github.com/ByteBarHQ)
