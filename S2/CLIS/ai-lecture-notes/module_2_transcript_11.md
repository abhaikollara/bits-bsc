# Linux Networking Commands — Cheatsheet
#hashtags: #networking #linux #hostname #ping #traceroute #nmap #ICMP #TCP #UDP #ports #diagnostics #TTL #RTT

---

## Title
Linux Networking Commands: hostname, ping, traceroute, Nmap — quick reference

---

## Key Definitions
- #hostname: command to display or set a system's network name (FQDN/short name).
- #ping: sends ICMP Echo Request to test reachability and measure round-trip time (RTT).
- #traceroute: traces network path (hops) from source to destination by manipulating TTL.
- #Nmap: network mapper — port/service scanner and discovery tool.
- #ICMP: Internet Control Message Protocol (used by ping).
- #TTL: Time To Live — hop-count limit for IP packets; used by traceroute.
- #RTT: Round-Trip Time — time for packet to go to host and return.

---

## Formulas / Notations
- RTT: measured per-packet by ping (typically shown in ms).
- TTL decrement → hop count (used by traceroute).
- ICMP Echo Request/Reply pair = connectivity check.
- localhost IP: 127.0.0.1
- Default ping packet payload on many Linux distros: 56 bytes data + 8 bytes ICMP header → 64 bytes total.

---

## Command Syntax Templates
- hostname: hostname [options] [new-hostname]
- ping: ping [options] destination
- traceroute: traceroute [options] destination
- nmap: nmap [scan-type options] [scan-options] target(s)

---

## Key Options / Quick Flag Reference

- hostname
  - -s : short hostname
  - -f : full/long hostname (FQDN)
  - -d : DNS domain name
  - -i : IP address of hostname
  - -I : all network addresses for host
  - (use man hostname for full list)  
  (#hostname)

- ping
  - -c <count> : send <count> packets then stop
  - -i <sec>   : interval between packets
  - -w <sec>   : deadline (max total seconds)
  - -s <size>  : data payload size (bytes)
  - Ctrl+C     : stop continuous ping (default on Linux runs until stopped)  
  (#ping #ICMP #RTT)

- traceroute
  - -n         : show numeric IPs (no DNS lookup)
  - -T         : use TCP packets (instead of default UDP/ICMP depending on platform)
  - -m <max>   : set maximum hops (max TTL)
  - (behavior) : increments TTL from 1 → max to elicit ICMP Time Exceeded replies to map hops  
  (#traceroute #TTL)

- Nmap
  - -sS : TCP SYN scan (fast, stealthy; half-open)
  - -sT : TCP connect scan (full TCP handshake)
  - -sU : UDP scan
  - -sV : service/version detection
  - -p <ports> : specify ports or ranges (e.g., -p 22,80,1000-2000)
  - -T<0..5> : timing template (0 slow → 5 aggressive)
  - <target> : hostname, IP, network (e.g., 192.168.1.0/24)  
  (LEGAL: only scan networks you own or have permission to scan)  
  (#nmap #ports #sS #sU #sV)

---

## Key Algorithms / Concepts (concise)
- Ping operation: send ICMP Echo Request → wait for Echo Reply → report RTT and packet loss (#ping #ICMP).
- Traceroute mechanism: send probes with increasing TTL; each router that decrements TTL to 0 returns ICMP Time Exceeded → reveals path & hop latency (#traceroute #TTL).
- Nmap scanning types:
  - SYN scan (-sS): send SYN, wait for SYN/ACK → determines open/closed without completing handshake.
  - Connect scan (-sT): full TCP connect() syscall; slower and more noisy.
  - UDP scan (-sU): send UDP packets; open/filtered detection is less reliable.
  - Version detection (-sV): probes services to identify software/version (#nmap).
- DNS resolution: hostnames map to IP via DNS; traceroute/ping may show hostname or numeric IP depending on flags (#DNS).

---

## Important Properties / Invariants
- Ping uses ICMP; some hosts/firewalls block ICMP → "host unreachable" or no replies.
- Traceroute depends on ICMP Time Exceeded responses; intermediate devices may drop/ignore probes or rate-limit responses.
- Nmap results can be affected by firewall rules, IDS/IPS, and host responsiveness — absence of responses ≠ guaranteed closed port.
- Changing hostname may require privileges and may not persist across reboots depending on distro/config.
- localhost = 127.0.0.1 (IPv4 loopback) — always local machine.
- Default ping on Linux sends packets continuously until stopped; use -c for fixed count.

---

## Quick Reference (one-liners & examples)
- Show hostname: hostname
- Show FQDN: hostname -f
- Show short name: hostname -s
- Show IP(s): hostname -i  (single)  | hostname -I (all)
- Ping once (4 packets): ping -c 4 example.com
- Ping every 5s: ping -i 5 8.8.8.8
- Ping with packet size 100 bytes: ping -s 100 host
- Trace route (numeric IPs): traceroute -n example.com
- Traceroute with TCP probes max 30 hops: traceroute -T -m 30 example.com
- Nmap quick SYN scan top ports: nmap -sS -T4 target
- Nmap UDP & version detection: nmap -sU -sV -p U:53,161 target
- Common ports: 21 FTP, 22 SSH, 23 Telnet, 25 SMTP, 53 DNS, 80 HTTP, 443 HTTPS, 3306 MySQL
- Legal reminder: Only scan authorized networks (Nmap usage can be illegal without permission).

---

## Where to get more info
- man hostname
- man ping
- man traceroute
- man nmap / nmap --help
- Nmap reference: https://nmap.org/book/quickstart.html

---

Keep this sheet for quick flags, command templates, and reminders about behavior (ICMP vs TCP/UDP, TTL behavior, permissions/legal).