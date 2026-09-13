# PowerShell Commands Cheat Sheet

> Core cmdlets, must-know aliases, and admin one-liners for Windows environments.

## The Pattern

Every cmdlet is **Verb-Noun**: `Get-Process`, `Stop-Service`, `New-Item`

## Must-Know Aliases

| Alias | Full cmdlet |
|---|---|
| `ls` / `dir` | `Get-ChildItem` |
| `cat` | `Get-Content` |
| `echo` | `Write-Output` |
| `ps` | `Get-Process` |
| `kill` | `Stop-Process` |
| `cp` | `Copy-Item` |
| `mv` | `Move-Item` |
| `rm` | `Remove-Item` |
| `man` | `Get-Help` |
| `?` | `Where-Object` |
| `%` | `ForEach-Object` |

## Files & System

```powershell
Get-ChildItem -Recurse -Filter *.log   # find files
Get-Content log.txt -Tail 20 -Wait     # live tail
Copy-Item src dst -Recurse
Get-Help Get-Process -Examples          # built-in examples
Get-Command *service*                  # discover cmdlets
```

## Processes & Services

```powershell
Get-Process | Sort-Object CPU -Descending | Select-Object -First 5
Stop-Process -Name notepad -Force
Get-Service | Where-Object {$_.Status -eq 'Running'}
Restart-Service -Name Spooler
```

## Networking

```powershell
Test-Connection 8.8.8.8 -Count 4          # ping
Test-NetConnection example.com -Port 443  # port check
Get-NetIPAddress                          # IP config
Get-DnsClientCache | Clear-DnsClientCache # flush DNS: Clear-DnsClientCache
Resolve-DnsName example.com               # nslookup equivalent
```

## Active Directory (RSAT / DC)

```powershell
Get-ADUser -Filter * -SearchBase "OU=Sales,DC=corp,DC=local"
Get-ADUser jdoe | Unlock-ADAccount
Set-ADAccountPassword jdoe -Reset
Get-ADComputer -Filter * | Select-Object Name,OperatingSystem
```

## Pipeline Power (exam + interview favorites)

```powershell
# Top 5 CPU hogs, names only:
Get-Process | Sort-Object CPU -Descending | Select-Object -First 5 Name

# Find large files:
Get-ChildItem C:\ -Recurse -ErrorAction SilentlyContinue |
  Where-Object {$_.Length -gt 100MB} |
  Sort-Object Length -Descending
```

## Quick Hits

- **Execution policy** blocking scripts? `Set-ExecutionPolicy RemoteSigned -Scope CurrentUser`
- Cmdlets output **objects**, not text — pipe freely
- `$_` = the current object in the pipeline

---
📘 Full Windows admin + PowerShell study guides: **[bytebarhq.com](https://bytebarhq.com)** — by [ByteBar](https://github.com/ByteBarHQ)
