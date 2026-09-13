# OSI Model Cheat Sheet

> All 7 layers, what lives at each, and the mnemonics that make them stick.

## The 7 Layers

| # | Layer | What it does | Protocols | Devices |
|---|---|---|---|---|
| 7 | **Application** | User-facing services | HTTP, FTP, SMTP, DNS, DHCP | — |
| 6 | **Presentation** | Data format, encryption, compression | TLS/SSL, JPEG, ASCII | — |
| 5 | **Session** | Connections between apps | NetBIOS, RPC, PPTP | — |
| 4 | **Transport** | End-to-end delivery, ports | **TCP, UDP** | Firewall (stateful) |
| 3 | **Network** | Routing, logical addressing | **IP, ICMP**, OSPF, BGP | **Router**, L3 switch |
| 2 | **Data Link** | Switch-to-switch, MAC addressing | Ethernet, ARP, PPP | **Switch**, bridge, NIC |
| 1 | **Physical** | Bits on the wire | — | Hub, repeater, cables |

## Mnemonics

- **Top → bottom:** *All People Seem To Need Data Processing*
- **Bottom → top:** *Please Do Not Throw Sausage Pizza Away*

## Data Names per Layer (encapsulation)

| Layer | Data unit |
|---|---|
| 4 Transport | **Segment** (TCP) / Datagram (UDP) |
| 3 Network | **Packet** |
| 2 Data Link | **Frame** |
| 1 Physical | **Bits** |

👉 Exam trick: "What PDU at Layer 3?" → **Packet**. Layer 2 → **Frame**. Layer 4 → **Segment**.

## TCP/IP Model vs OSI

| TCP/IP layer | Maps to OSI |
|---|---|
| Application | 7 + 6 + 5 (Application, Presentation, Session) |
| Transport | 4 (Transport) |
| Internet | 3 (Network) |
| Network Access | 2 + 1 (Data Link, Physical) |

## Quick Exam Hits

- **ARP** works at Layer 2/3 boundary (resolves IP → MAC)
- **TLS** lives at Layer 6 (Presentation)
- **Switches** = Layer 2 (MAC addresses) · **Routers** = Layer 3 (IP addresses)
- **MTU** issues and fragmentation → Layer 3

---
📘 Full networking fundamentals + practice questions: **[bytebarhq.com](https://bytebarhq.com)** — by [ByteBar](https://github.com/ByteBarHQ)
