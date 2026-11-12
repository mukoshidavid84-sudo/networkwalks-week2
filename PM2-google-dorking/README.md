# Week 2 - Project Module 2: OSINT & Google Dorking Reconnaissance
**Program:** NETWORK WALKS — Cybersecurity Internship 2026  
**Author:** David Mukoshi  
**Methodology:** Google Dorking (Advanced Search Operators)  

---

## Overview
This module demonstrates Open Source Intelligence (OSINT) reconnaissance using Google Dork operators to identify publicly exposed network camera interfaces and open-access mathematics PDF resources across educational domains and open directory indexes.

---

## Task 1: 10 Exposed Security Camera Links & Relevant Dorks

| # | Camera Link | Relevant Google Dork | Default Username | Default Password |
| :--- | :--- | :--- | :--- | :--- |
| 1 | `http://122.116.41.8:8080` | `intitle:"webcamXP" inurl:":8080"` | None | None |
| 2 | `http://109.233.191.130:8080` | `intitle:"webcamXP 5"` | None | None |
| 3 | `http://88.34.237.193:81` | `inurl:"control/userimage.html"` | None | None |
| 4 | `http://80.152.138.183/viewerframe?mode=refresh` | `inurl:"viewerframe?mode="` | None | None |
| 5 | `http://191.96.127.25:8081` | `intitle:"Network Camera NetworkCamera"` | None | None |
| 6 | `http://139.64.168.126:8080` | `inurl:"cam_1.cgi"` | None | None |
| 7 | `http://95.255.183.164:8080` | `inurl:"cam_1.cgi"` | None | None |
| 8 | `http://109.206.96.75:8080` | `inurl:"cam_1.cgi"` | None | None |
| 9 | `http://89.207.169.237:8004` | `intitle:"Network Camera NetworkCamera"` | None | None |
| 10 | `http://213.129.132.171/viewerframe?mode=refresh` | `inurl:"viewerframe?mode="` | None | None |

### Supporting Evidence
* **`01_insecam_live_camera.png`:** Live camera feed observed at `http://139.64.168.126:8080` (`inurl:"cam_1.cgi"`).
* **`02_insecam_live_camera.png`:** Insecam directory interface showing publicly indexed unauthenticated streams.

---

## Task 2: 10 Downloadable Mathematics Ebooks (PDF Format)

| # | Resource Title / Subject | Relevant Google Dork | File Type |
| :--- | :--- | :--- | :--- |
| 1 | Elementary Calculus Textbook | `site:edu filetype:pdf "Calculus" intitle:"index of"` | PDF |
| 2 | Linear Algebra & Applications | `site:edu filetype:pdf "Linear Algebra" intitle:"index of"` | PDF |
| 3 | Ordinary Differential Equations | `filetype:pdf "Differential Equations" intitle:"index of"` | PDF |
| 4 | Probability & Statistics Manual | `site:edu filetype:pdf "Probability and Statistics"` | PDF |
| 5 | Discrete Mathematics Notes | `filetype:pdf "Discrete Mathematics" intitle:"index of"` | PDF |
| 6 | Abstract Algebra Essentials | `site:edu filetype:pdf "Abstract Algebra" "lecture notes"` | PDF |
| 7 | Principles of Real Analysis | `filetype:pdf "Real Analysis" intitle:"index of"` | PDF |
| 8 | Introduction to Topology | `site:edu filetype:pdf "Topology" "lecture notes"` | PDF |
| 9 | Elementary Number Theory | `filetype:pdf "Number Theory" intitle:"index of"` | PDF |
| 10 | Complex Variables & Analysis | `site:edu filetype:pdf "Complex Analysis"` | PDF |

---

## Remediation Recommendations
* **Network Segmentation & Access Control:** Place IP cameras behind a firewall/VLAN, enforce strong authentication, and require VPN access.
* **Search Engine Indexing Prevention:** Configure `robots.txt` (`User-agent: * Disallow: /`) and authentication headers on sensitive web interfaces.
