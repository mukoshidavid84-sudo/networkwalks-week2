
# Week 2 - Project Module 5: Network Scanning & Host Discovery with Zenmap
**Program:** NETWORK WALKS — Cybersecurity Internship 2026  
**Author:** David Mukoshi  
**Target Subnet:** `192.168.0.0/24`  
**Environment:** Windows (Zenmap & Command Prompt)  

---

## Overview
This module demonstrates local network discovery and active host enumeration using **Zenmap** (the official Nmap GUI) on Windows. By determining the local IPv4 subnet via `ipconfig` and executing a Ping Scan (`nmap -sn 192.168.0.0/24`), live hosts, response latencies, and hardware MAC addresses on the local area network (LAN) were identified.

---

## Step-by-Step Execution & Specific Findings

### Task 1: Subnet Identification & Target Configuration (`zenmap1`)
* **Action:** Installed Zenmap on Windows and executed `ipconfig` in Command Prompt to identify the local host IP (`192.168.0.229`), default gateway (`192.168.0.1`), and `/24` subnet mask.
* **Configuration:** Entered `192.168.0.0/24` into the Zenmap **Target** field and selected the **Ping Scan** profile (`nmap -sn 192.168.0.0/24`).
* **Evidence:** Saved screenshot as `zenmap1`.

### Task 2: Live Host Enumeration & Scan Output (`zenmap2`)
* **Command Executed:** `nmap -sn 192.168.0.0/24`
* **Scan Summary:** `Nmap done: 256 IP addresses (2 hosts up) scanned in 3.31 seconds`

#### Discovered Live Hosts

| IP Address | Role / Identification | Status & Latency | MAC Address |
| :--- | :--- | :--- | :--- |
| `192.168.0.1` | Default Gateway / Router | Up (`0.0014s` latency) | `EC:B9:31:57:95:48` (Unknown) |
| `192.168.0.229` | Local Host PC | Up | Local Interface |

#### Raw Scan Report Highlights
```text
Nmap scan report for 192.168.0.1
Host is up (0.0014s latency).
MAC Address: EC:B9:31:57:95:48 (Unknown)

Nmap scan report for 192.168.0.229
Host is up.

Nmap done: 256 IP addresses (2 hosts up) scanned in 3.31 seconds
