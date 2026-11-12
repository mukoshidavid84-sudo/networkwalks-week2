
# Week 2 - Project Module 4: OSINT Enumeration with theHarvester
**Program:** NETWORK WALKS — Cybersecurity Internship 2026  
**Author:** David Mukoshi  
**Target Domain:** `microsoft.com`  
**Environment:** Kali Linux  

---

## Overview
This module demonstrates passive Open Source Intelligence (OSINT) gathering using **theHarvester** in Kali Linux to enumerate subdomains, hosts, IP addresses, and public email addresses associated with `microsoft.com` across public search engines and data sources.

---

## Step-by-Step Execution & Commands

### Task 1: Targeted Search Engine Enumeration (`harvester1`)
* **Command:** `theHarvester -d microsoft.com -l 1000 -b baidu`
* **Flag Breakdown:**
  * `-d microsoft.com`: Sets the target domain to enumerate.
  * `-l 1000`: Limits the search to the first 1,000 results.
  * `-b baidu`: Specifies Baidu as the OSINT data source.
* **Evidence:** Saved screenshot as `harvester1`.

### Task 2: Multi-Source Enumeration & Output Logging (`harvester2`)
* **Command:** `theHarvester -d microsoft.com -l 50 -b all`
* **Flag Breakdown:**
  * `-d microsoft.com`: Sets the target domain.
  * `-l 50`: Limits results to 50 entries per source.
  * `-b all`: Queries all available passive OSINT data sources simultaneously.
* **Evidence:** Saved screenshot as `harvester2` and exported raw enumeration output to a `.txt` log file.
