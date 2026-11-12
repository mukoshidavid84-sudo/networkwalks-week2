# Week 2 - Project Module 1: Passive & Active Web Reconnaissance
**Program:** NETWORK WALKS — Cybersecurity Internship 2026  
**Author:** David Mukoshi  
**Target Domain:** `networkwalks.com`  
**Environment:** Kali Linux  

---

## Overview
This module documents passive and active reconnaissance performed against `networkwalks.com` to gather domain registration details, hosting infrastructure, DNS records, HTTP response headers, web technologies, and Web Application Firewall (WAF) protections.

---

## Step-by-Step Execution & Findings

### 1. WHOIS Domain Lookup (`01_whois.png`)
* **Command:** `whois networkwalks.com`
* **Findings:** Registered via GoDaddy.com, LLC (IANA ID: 146) from Nov 6, 2019 to Nov 6, 2027. Name servers point to `NS6135.HOSTGATOR.COM` and `NS6136.HOSTGATOR.COM` with DNSSEC unsigned and client transfer/delete locks enabled.

### 2. Web Technology Fingerprinting (`02_whatweb.png`)
* **Command:** `whatweb networkwalks.com`
* **Findings:** Runs on Apache (redirecting HTTP `301` to HTTPS `200 OK`), powered by WordPress 7.1.4, WordPress Download Manager 3.3.76, Bootstrap 7.1.4, and jQuery 3.7.1. Hosted in the US (`192.232.216.135`) with public contact `info@networkwalks.com`.

### 3. DNS Resolution (`03_nslookup.png`)
* **Command:** `nslookup networkwalks.com`
* **Findings:** Resolved `networkwalks.com` to IPv4 A record `192.232.216.135`.

### 4. HTTP Response Headers (`04_curl_headers.png`)
* **Command:** `curl -I https://networkwalks.com`
* **Findings:** Confirmed `HTTP/2 200` on an Apache server with Nginx WordPress caching (`x-nginx-cache: WordPress`), `permissions-policy`, `referrer-policy`, and `HttpOnly`/`Secure` flags on the `__wpdm_client` cookie.

### 5. Web Application Firewall Detection (`05_wafw00f.png`)
* **Command:** `wafw00f networkwalks.com`
* **Findings:** Confirmed `https://networkwalks.com` is protected behind **ModSecurity (SpiderLabs) WAF**.

### 6. Comprehensive DNS Enumeration (`06_dnsrecon.png`)
* **Command:** `dnsrecon -d networkwalks.com`
* **Findings:** Enumerated 8 DNS records including SOA (`ns6135.hostgator.com`), NS (`ns6136.hostgator.com`), MX (`mail.networkwalks.com`), TXT (SPF policy and Google site verification), and cPanel autodiscover SRV records.
