# Network Reconnaissance & Automated Vulnerability Scanner

![Bash](https://img.shields.io/badge/Language-Bash-4EAA25?style=flat&logo=gnu-bash&logoColor=white)
![Nmap](https://img.shields.io/badge/Tool-Nmap-00599C?style=flat&logo=nmap&logoColor=white)
![Security](https://img.shields.io/badge/Category-Red%20Team%20%2F%20Pentesting-red)

## 📌 Overview
This repository contains a practical cybersecurity laboratory guide and an automated Bash script (`auto-recon.sh`) designed for active reconnaissance, port scanning, service version enumeration, and vulnerability identification using **Nmap**, **Vulners API**, and **Vulscan (offline mode)**.

The project demonstrates network auditing methodologies applied across isolated environments (Metasploitable2,) within VirtualBox.

---

## 🛠️ Key Features.
- **Network Fundamentals & Protocol Analysis**: Deep dive into OSI vs TCP/IP models, TCP 3-way handshake, ARP resolution, and routing diagnostics via Traceroute.
- **Port Scanning & Banner Grabbing**: Execution of SYN Stealth scans, UDP scanning, and manual verification using `netcat` and `telnet`.
- **Dual Vulnerability Engine Integration**:
  - **Online**: Live API vulnerability lookup via `vulners.nse`.
  - **Offline/Air-Gapped**: Local correlation using `vulscan.nse` with offline ExploitDB CSV databases.
- **Automated Script Execution**: `auto-recon.sh` streamlines Phase 1 (Reconnaissance) and Phase 2 (Vulnerability Correlation) into formatted output reports.

---

## 🚀 Usage (`auto-recon.sh`)

### Prerequisites
Make sure Nmap, Vulners, and Vulscan are installed on Kali Linux:
```bash
# Clone Vulscan repository into Nmap scripts directory
cd /usr/share/nmap/scripts/
sudo git clone [https://github.com/scipag/vulscan.git](https://github.com/scipag/vulscan.git)
sudo nmap --script-updatedb