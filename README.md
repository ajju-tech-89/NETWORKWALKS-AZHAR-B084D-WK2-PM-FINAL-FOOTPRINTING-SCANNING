
# Cybersecurity & Ethical Hacking – Week 2 Project

## 📌 Project Overview

This repository contains my Week 2 practical work for the Cybersecurity & Ethical Hacking internship with **Networkwalks**.

The main objective of this project was to understand reconnaissance techniques, open-source intelligence (OSINT), and network discovery using industry-standard cybersecurity tools.

The project focuses on collecting information, identifying network assets, and documenting findings through practical exercises.

---

## 🎯 Project Objectives

- Understand website footprinting techniques.
- Explore publicly available information using OSINT.
- Identify live hosts within a network.
- Analyze IP addresses and available MAC addresses.
- Visualize network topology using Zenmap.
- Document practical activities with screenshots and command outputs.

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|---|---|
| Kali Linux | Security testing environment |
| WHOIS | Domain registration information |
| WhatWeb | Website technology identification |
| NSLookup | DNS lookup |
| cURL | HTTP header inspection |
| WAFW00F | Web Application Firewall detection |
| DNSRecon | DNS information gathering |
| theHarvester | OSINT and information gathering |
| Zenmap | Network discovery and visualization |
| Nmap | Network scanning engine |
| Windows CMD | Local network configuration |

---

## 🔍 Project Modules

### Module 1 – Website Footprinting (PM1)

Performed website footprinting using multiple Kali Linux tools.

**Practical Tasks:**

- WHOIS – Collected domain registration details.
- WhatWeb – Identified website technologies.
- NSLookup – Retrieved DNS information.
- cURL – Examined HTTP response headers.
- WAFW00F – Checked for Web Application Firewall presence.
- DNSRecon – Gathered DNS records.

**Target:** `networkwalks.com`

**Evidence:** Screenshots and command outputs.

---

### Module 2 – OSINT with theHarvester (PM4)

Used theHarvester to collect publicly available information from different search sources.

**Practical Tasks:**

**Task 1:**
- Target domain: `microsoft.com`
- Source: Baidu
- Result limit: 1000
- Collected publicly available email addresses and hostnames.

**Task 2:**
- Target domain: `microsoft.com`
- Source: All supported sources
- Result limit: 50
- Compared the information returned by different sources.

**Learning:** Search sources may provide different results, and some sources require API keys.

---

### Module 3 – Network Scanning with Zenmap (PM5)

Used Zenmap on Windows to discover active devices within my local lab network.

**Practical Tasks:**

1. Downloaded and installed Zenmap.
2. Identified the local IP address and LAN subnet.
3. Performed a Ping Scan to discover live hosts.
4. Counted the active hosts.
5. Identified the IP addresses of discovered hosts.
6. Checked available MAC addresses.
7. Generated and saved the network topology as a PDF.

**Evidence:** Zenmap screenshots, scan results, and topology PDF.

---

## 📂 Repository Structure

```text
Week-2-Cybersecurity-Project/
│
├── Docs
     |───PM 1.docx
     |───PM 4.docx
     |───PM 5 Topology.pdf
├── Report
     |───Penetration_Testing_Report_W2-PM
├── Screenshots
     |───PM1 Task 1 Whois.png
     |───PM1 Task 2 What web.png
     |───PM1 Task 3 NSLOOKUP.png
     |───PM1 Task 4 CURL.png
     |───PM1 Task 5 WAFW00F.png
     |───PM1 Task 6 DNSRECON.png
     |───PM4 TASK 2 All.png
     |───PM4 Task 1 Baidu.png
     |───PM5 IP sacn.png
     |───PM5 IP.png
     |───PM5 Topology pdf.png
     |───PM5 Topology.png
|
└─README.md
```

---

## 💡 Key Learnings

- Understanding the importance of reconnaissance in cybersecurity.
- Learning how to use multiple tools for information gathering.
- Exploring OSINT techniques and publicly available data.
- Discovering live hosts within a local network.
- Understanding network topology and device identification.
- Improving technical documentation and reporting skills.

---

## 🔐 Ethical Considerations

All practical activities were conducted within the assigned project scope and authorized environments.

This project focuses on ethical learning, responsible information gathering, and proper documentation.

---

## 🙏 Acknowledgement

I would like to thank **Waqas Karim CCIE** and the **Networkwalks** team for providing this practical learning opportunity and helping me develop my cybersecurity skills.

---

<p align="center">
  <strong>Author: [Azhar Mansuri], Cybersecurity Intern, Networkwalks (B084D) </strong>
  <br>
  Learning • Practicing • Documenting
</p>
