
# Week 2 - Project Module 3: OSINT & Link Analysis with Maltego
**Program:** NETWORK WALKS — Cybersecurity Internship 2026  
**Author:** David Mukoshi  
**Target Domain:** `networkwalks.com`  
**Tool Used:** Maltego Graph (Desktop) v4.14.0  

---

## Overview
This module demonstrates graphical Open Source Intelligence (OSINT) and entity link analysis using **Maltego**. The objective was to set up the Maltego environment, map a target domain entity (`networkwalks.com`), and execute automated transforms to discover publicly associated email addresses.

---

## Step-by-Step Execution & Explanation

### 1. Maltego Installation & Activation (`01_maltego_install.png`)
* Downloaded and installed **Maltego Graph (Desktop) v4.14.0** with administrative privileges.
* Completed the OAuth login and **Maltego ID Activation** wizard to unlock standard OSINT data sources and transforms.

### 2. Domain Mapping & Email Enumeration (`02_maltego_domain_email_transform.png`)
* Created a new investigation graph and dragged a **Domain** entity from the Entity Palette onto the workspace, setting the target to `networkwalks.com`.
* Executed the **`To Emails @domain [Search Engine]`** and **`To Email address [From whois info]`** transforms on the domain node.
* **Result:** Maltego mapped a direct relationship arrow pointing from `networkwalks.com` to the discovered email entity **`info@networkwalks.com`**, confirming a publicly exposed administrative contact address for the domain.
