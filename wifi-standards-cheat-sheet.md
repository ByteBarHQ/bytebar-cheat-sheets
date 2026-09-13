# Wi-Fi Standards Cheat Sheet (802.11)

> Frequencies, speeds, and ranges — Network+ and CCNA wireless in one page.

## Standards Table

| Standard | Branding | Frequency | Max Speed | Range (indoor) |
|---|---|---|---|---|
| 802.11a | — | 5 GHz | 54 Mbps | ~35 m |
| 802.11b | — | 2.4 GHz | 11 Mbps | ~38 m |
| 802.11g | — | 2.4 GHz | 54 Mbps | ~38 m |
| 802.11n | Wi-Fi 4 | 2.4 / 5 GHz | 600 Mbps | ~70 m |
| 802.11ac | Wi-Fi 5 | 5 GHz | ~3.5 Gbps | ~35 m |
| 802.11ax | Wi-Fi 6/6E | 2.4 / 5 / 6 GHz | ~9.6 Gbps | ~35 m |
| 802.11be | Wi-Fi 7 | 2.4 / 5 / 6 GHz | ~46 Gbps | ~35 m |

## 2.4 GHz vs 5 GHz vs 6 GHz

| | 2.4 GHz | 5 GHz | 6 GHz |
|---|---|---|---|
| Range / wall penetration | Best | Medium | Worst |
| Speed | Slowest | Fast | Fastest |
| Congestion | Worst (only 3 non-overlapping channels) | Better | Cleanest |

**Non-overlapping 2.4 GHz channels:** **1, 6, 11** (US) — exam favorite.

## Wireless Security (oldest → newest)

| Protocol | Status |
|---|---|
| WEP | **Broken** — crackable in minutes, never use |
| WPA | Deprecated — TKIP flaws |
| WPA2 | Minimum acceptable (AES-CCMP) |
| WPA3 | Current standard (SAE handshake) |

## Quick Exam Hits

- **MIMO** (multiple antennas) arrived with **802.11n**
- **MU-MIMO** (multiple users at once) arrived with **802.11ac**
- **OFDMA** (efficient channel sharing) arrived with **802.11ax / Wi-Fi 6**
- **SSID** = network name · **Rogue AP** = unauthorized access point (evil twin risk)
- Enterprise auth = **802.1X** with **RADIUS** server

---
📘 Full wireless networking + practice questions: **[bytebarhq.com](https://bytebarhq.com)** — by [ByteBar](https://github.com/ByteBarHQ)
