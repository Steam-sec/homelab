# Home Lab — IT & System Administration Practice

A hands-on home lab I built from spare and secondhand machines to practice system administration, networking, and security skills — the same material I'm studying in the Google IT Support Professional Certificate (Course 4: *System Administration and IT Infrastructure Services*).

Every lab is documented the same way: what I set out to do, why, the problems I hit, and how I resolved them.

## The Fleet

| Machine | OS / Role |
|---|---|
| 2009 MacBook Pro | **Kali Linux** — security & packet analysis |
| 2012 MacBook Air | **Zorin OS** — Linux productivity & planned services host |
| 2012 MacBook Air | **Linux Mint** — Apache web-server lab |
| Gaming PC | **Windows** — main workstation & build project |
| Unmanaged switch | Lab network interconnect (standby) |
| ARRIS SBG8300 | Home gateway |

## What I've Done Here

- **Linux rescue & recovery** — recovered a Kali install from a broken 713-package upgrade: cleared a stuck dpkg lock, repaired the package state, and hot-swapped the window manager (XFWM4 → Metacity) mid-repair to keep the GUI alive
- **Web server build** — Apache on Linux Mint: DNS resolver fixes, IPv4 forcing, UFW firewall rules, verified with `curl -I`
- **DNS & packet analysis** — Wireshark captures on port 53; proved the router was passing queries through by comparing `nslookup` against 8.8.8.8
- **Networking labs (Cisco Packet Tracer)** — star topology on a 2960 switch, static addressing, ICMP/ping analysis, crossover peer-to-peer, STP, VLANs, ARP behavior
- **Home network audit** — latency and route tracing across my ISP's network; TCP handshake and HTTP-vs-TLS audits
- **PC build & troubleshooting** — full platform upgrade (i7-7700K → i7-13700F, new motherboard, fresh OS); diagnosed XMP boot-loops with CMOS resets and stabilized DDR at 3200 MT/s

## Documentation

📓 **[labs-notes.md](labs-notes.md)** — the full lab notebook: write-ups, runbooks (clock desync/NTP, broken repositories, full disk, GUI crash recovery, Wireshark filters), a startup checklist, an error cheat sheet, and a case study mapping these labs to the Google IT Support syllabus.

## Planned Next

- SSH headless administration + Ansible basics on the Mint server
- Docker/Portainer, Nginx, and Pi-hole on the Zorin machine
- Python disk-health monitoring script
- Tailscale/WireGuard remote access
