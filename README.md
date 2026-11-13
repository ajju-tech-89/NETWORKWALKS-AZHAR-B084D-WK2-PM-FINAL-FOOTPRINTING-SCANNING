
# WEEK 2 – CYBERSECURITY & ETHICAL HACKING PROJECT

<p align="center">
  <strong>NETWORKWALKS | Cybersecurity Internship</strong>
</p>

<p align="center">
  <em>Footprinting • OSINT • Network Scanning</em>
</p>

---

## 📌 Project Overview

This repository documents my practical work completed during Week 2 of the Cybersecurity & Ethical Hacking Internship with **Networkwalks**.

The objective of this project was to understand the initial stages of a cybersecurity assessment, including information gathering, website footprinting, Open-Source Intelligence (OSINT), and network discovery.

Throughout the project, I worked with different cybersecurity tools in Kali Linux and Windows to collect information, examine network services, identify active hosts, and understand network topology.

The repository contains practical tasks, command outputs, screenshots, observations, and supporting documentation for the completed project modules.

---

## 📑 Table of Contents

1. [Project Objectives](#-project-objectives)
2. [Tools and Technologies](#-tools-and-technologies)
3. [Project Modules](#-project-modules)
   - [PM1 – Website Footprinting](#module-1-pm1--website-footprinting)
   - [PM4 – OSINT with theHarvester](#module-2-pm4--osint-with-theharvester)
   - [PM5 – Network Scanning with Zenmap](#module-3-pm5--network-scanning-with-zenmap)
4. [Results and Observations](#-results-and-observations)
5. [Glossary](#-glossary)
6. [Key Learnings](#-key-learnings)
7. [Risk Analysis and Limitations](#-risk-analysis-and-limitations)
8. [Ethical Considerations](#-ethical-considerations)
9. [Project Summary](#-project-summary)
10. [Repository Structure](#-repository-structure)
11. [Acknowledgement](#-acknowledgement)

---

## 🎯 Project Objectives

The main objectives of this project were:

- Understand the fundamentals of website footprinting.
- Gather domain and DNS-related information using Kali Linux tools.
- Identify website technologies and inspect HTTP headers.
- Understand Web Application Firewall detection.
- Perform OSINT using theHarvester.
- Collect publicly available email addresses and hostnames.
- Discover active devices within a local network.
- Identify IP addresses and available MAC addresses.
- Visualize network connections using Zenmap.
- Maintain proper screenshots and command-output documentation.

---

## 🛠️ Tools and Technologies

| Tool | Purpose |
|---|---|
| Kali Linux | Cybersecurity testing environment |
| WHOIS | Domain registration information |
| WhatWeb | Website technology identification |
| NSLookup | DNS lookup and IP information |
| cURL | HTTP request and header inspection |
| WAFW00F | Web Application Firewall detection |
| DNSRecon | DNS information gathering |
| theHarvester | OSINT and information gathering |
| Zenmap | Graphical network scanning |
| Nmap | Network discovery and scanning engine |
| Windows CMD | Local network configuration |

---

# 🔍 Project Modules

## Module 1: PM1 – Website Footprinting

### Introduction

Website footprinting is an information-gathering technique used to understand the publicly available information associated with a website or domain.

In this module, different Kali Linux tools were used to examine domain registration information, website technologies, DNS records, HTTP headers, and possible Web Application Firewall protection.

**Target Domain:** `networkwalks.com`

### Tasks Performed

#### Task 1 – WHOIS Lookup

**Command:**
```bash
whois networkwalks.com
```

**Purpose:**
To collect publicly available domain registration information, such as registrar details, registration dates, and name servers.

#### Task 2 – Website Technology Detection

**Command:**
```bash
whatweb networkwalks.com
```

**Purpose:**
To identify technologies and services that may be used by the target website.

#### Task 3 – DNS Lookup

**Command:**
```bash
nslookup networkwalks.com
```

**Purpose:**
To retrieve DNS information and identify the IP address associated with the domain.

#### Task 4 – HTTP Header Inspection

**Command:**
```bash
curl -I https://networkwalks.com
```

**Purpose:**
To inspect HTTP response headers and understand how the web server responds to requests.

#### Task 5 – WAF Detection

**Command:**
```bash
wafw00f networkwalks.com
```

**Purpose:**
To check whether a Web Application Firewall can be identified on the target website.

#### Task 6 – DNS Enumeration

**Command:**
```bash
dnsrecon -d networkwalks.com
```

**Purpose:**
To gather DNS-related information and identify available DNS records.

### Module Outcome

This module provided practical experience with multiple footprinting tools and demonstrated how different sources of information can help build an initial picture of a website's public-facing infrastructure.

**Evidence:** Screenshots and saved command outputs.

---

## Module 2: PM4 – OSINT with theHarvester

### Introduction

Open-Source Intelligence (OSINT) involves collecting and analyzing information from publicly available sources.

In this module, theHarvester was used to search for publicly available email addresses and hostnames associated with a target domain.

**Target Domain:** `microsoft.com`

### Task 1 – Information Gathering Using Baidu

**Command:**
```bash
theHarvester -d microsoft.com -l 1000 -b baidu
```

**Command Explanation:**

- `theHarvester` – Starts the information-gathering tool.
- `-d` – Specifies the target domain.
- `microsoft.com` – Target domain.
- `-l 1000` – Sets the result limit to 1000.
- `-b baidu` – Uses Baidu as the search source.

**Objective:**

To collect publicly available email addresses and hostnames related to the target domain using Baidu.

### Task 2 – Information Gathering Using All Sources

**Command:**
```bash
theHarvester -d microsoft.com -l 50 -b all
```

**Command Explanation:**

- `-d` – Specifies the target domain.
- `-l 50` – Sets the result limit to 50.
- `-b all` – Requests all sources supported by the installed version.

**Objective:**

To gather information using multiple available sources and compare the results.

### Module Outcome

This module provided practical understanding of OSINT and automated information gathering.

It also demonstrated that search results may vary depending on the source, available data, and API-key requirements.

**Evidence:** Screenshots and saved command outputs for both tasks.

---

## Module 3: PM5 – Network Scanning with Zenmap

### Introduction

Zenmap is the graphical user interface for Nmap. It helps users perform network discovery and visualize scan results.

In this module, Zenmap was used on Windows to identify active devices within a local network and generate a network topology map.

### Tasks Performed

#### Task 1 – Download and Install Zenmap

Downloaded Zenmap from the official Nmap website and completed the installation on Windows.

Official Website: https://nmap.org/download.html

#### Task 2 – Find Local IP Address and LAN Subnet

**Command:**
```cmd
ipconfig
```

Used Windows Command Prompt to identify:

- IPv4 Address
- Subnet Mask
- Default Gateway

The local subnet was determined using the network configuration.

#### Task 3 – Discover Live Hosts

Opened Zenmap, entered the local LAN subnet, selected the **Ping Scan** profile, and performed a network discovery scan.

**Purpose:**

To identify active devices within the local network.

#### Task 4 – Count Live Hosts

Examined the Zenmap scan results to determine the number of active hosts.

**Observed Result:** 3 live hosts were reported in the scan.

#### Task 5 – Identify IP Addresses

Recorded the IP addresses of the discovered live hosts from the scan results.

#### Task 6 – Identify MAC Addresses

Examined available MAC address information for the discovered devices.

For the local Windows machine, the following command was used:

```cmd
ipconfig /all
```

The Physical Address field was used to identify the local network adapter's MAC address.

#### Task 7 – Generate Network Topology PDF

Opened the Topology tab in Zenmap, enabled the legend, reviewed the network map, and exported the topology graphic in PDF format.

### Module Outcome

This module provided practical experience in network discovery, active-host identification, IP and MAC address examination, and network topology visualization.

**Evidence:** Zenmap screenshots, scan results, and exported topology PDF.

---

## 📊 Results and Observations

| Module | Practical Work | Output |
|---|---|---|
| PM1 | Website footprinting | Domain, DNS, technology and HTTP information |
| PM4 | OSINT with theHarvester | Publicly available emails and hostnames |
| PM5 | Network scanning with Zenmap | Live hosts, IP/MAC information and topology PDF |

### General Observations

- Different tools provide different types of information.
- Public information can reveal useful details about an organization's digital footprint.
- OSINT results depend on the search source and its availability.
- Network scanning helps identify active devices within a subnet.
- A discovered service or information point does not automatically indicate a security vulnerability.

---

## 📖 Glossary

| Term | Description |
|---|---|
| Footprinting | Collecting information about a target before security assessment. |
| Reconnaissance | Initial information-gathering phase of a security assessment. |
| OSINT | Open-Source Intelligence; collecting information from public sources. |
| WHOIS | A protocol used to retrieve domain registration information. |
| DNS | Domain Name System, which translates domain names into IP addresses. |
| IP Address | A logical address used to identify a device on a network. |
| MAC Address | A hardware-level network interface address. |
| HTTP Headers | Metadata exchanged between a client and web server. |
| WAF | Web Application Firewall, used to filter and monitor web traffic. |
| Subnet | A logical division of an IP network. |
| Live Host | A device that responds to a network discovery check. |
| Ping Scan | A network discovery method used to identify active hosts. |
| Nmap | A network scanning and discovery tool. |
| Zenmap | The graphical interface for Nmap. |
| Network Topology | A visual representation of devices and their network connections. |
| Enumeration | Collecting detailed information about discovered systems and services. |

---

## 💡 Key Learnings

During this week's practical activities, I learned:

1. How to perform basic website footprinting using multiple Kali Linux tools.
2. How to collect domain registration and DNS information.
3. How to identify website technologies and inspect HTTP headers.
4. How to check for possible Web Application Firewall protection.
5. How to use theHarvester for OSINT and public information gathering.
6. Why different search sources can produce different results.
7. How to discover active devices using Zenmap and Nmap.
8. How to identify IP addresses and available MAC addresses.
9. How to understand and export a network topology map.
10. Why proper documentation and authorization are essential in cybersecurity.

---

## ⚠️ Risk Analysis and Limitations

### Potential Risks

- Publicly available domain information may reveal infrastructure details.
- Exposed email addresses and hostnames may increase phishing and reconnaissance risks.
- Network scanning can generate traffic and may trigger security alerts.
- Incorrect interpretation of scan results can lead to misleading conclusions.
- Unapproved scanning or information gathering may violate organizational policies or laws.

### Limitations

- WHOIS and DNS information may not reveal every infrastructure detail.
- WhatWeb and WAFW00F results depend on the information exposed by the target.
- theHarvester results depend on available search sources and API access.
- Some devices may not respond to Ping Scan.
- MAC addresses may not be available for every discovered host, especially across routed networks.
- Scan results represent observations at the time of testing and may change.

### Risk Mitigation

- Perform testing only within an authorized scope.
- Use a controlled lab environment for network scanning.
- Avoid unauthorized access or intrusive testing.
- Verify information using multiple sources.
- Record unavailable or unconfirmed results honestly.
- Keep screenshots and outputs for proper documentation.

---

## 🔐 Ethical Considerations

Cybersecurity testing must always be performed responsibly.

All practical activities should remain within the assigned project scope, authorized targets, and permitted lab environments.

The information gathered during these exercises is intended for educational purposes and security awareness.

No unauthorized access or exploitation is intended.

---

## 📝 Project Summary

Week 2 provided practical exposure to three important areas of cybersecurity:

- **Website Footprinting:** Understanding domain information, website technologies, DNS, HTTP headers, and WAF detection.
- **OSINT:** Gathering publicly available information using theHarvester.
- **Network Scanning:** Discovering live devices and understanding network topology using Zenmap.

These activities helped build a foundation in reconnaissance, information gathering, and network discovery.

The project also highlighted the importance of verifying findings, understanding tool limitations, documenting observations, and following ethical security practices.

---

## 📂 Repository Structure

```text
WEEK-2-CYBERSECURITY-PROJECT/
│
├── PM1-Website-Footprinting/
│   ├── Screenshots/
│   └── Command-Outputs/
│
├── PM4-theHarvester/
│   ├── Screenshots/
│   └── Command-Outputs/
│
├── PM5-Zenmap-Network-Scanning/
│   ├── Screenshots/
│   ├── Scan-Results/
│   └── Network-Topology.pdf
│
├── Final-Report/
│
└── README.md
```

---

## 🙏 Acknowledgement

I would like to express my gratitude to **Waqas Karim CCIE** and the entire **Networkwalks** team for providing this practical learning opportunity.

This internship has helped me improve my understanding of cybersecurity tools, reconnaissance techniques, OSINT, and network scanning.

---

<p align="center">
  <strong>NETWORKWALKS – WEEK 2 PROJECT</strong>
  <br>
  Cybersecurity & Ethical Hacking Internship
  <br><br>
  <em>Learn • Practice • Analyze • Secure</em>
</p>
