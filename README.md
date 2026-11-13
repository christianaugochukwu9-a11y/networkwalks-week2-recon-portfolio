# Week 2: Footprinting, OSINT & Network Scanning Suite

## Ethical & Legal Disclaimer
All reconnaissance commands, Google Dorks, OSINT transforms, and Zenmap network scans documented in this repository were conducted strictly within authorized educational lab environments provided by Networkwalks Academy (`networkwalks.com`, `microsoft.com` public passive OSINT, and authorized lab targets). No intrusive exploitation or unauthorized system modifications were performed.

---

## Project Overview
This repository documents the complete execution of **Week 2** of my Cybersecurity & Ethical Hacking internship. Rather than completing only the minimum single elective required, I completed **all four Elective modules (W2-PM1 – W2-PM4)** as well as **both mandatory Essential modules (W2-PM5 & W2-PM-FINAL)**, establishing a full-spectrum workflow spanning passive OSINT, Google Hacking, graphical link analysis, CLI enumeration, and active network scanning.

---

## Completed Modules Matrix (6/6)

| Module ID | Category | Module Title | Core Tools / Techniques | Primary Target(s) |
| :--- | :--- | :--- | :--- | :--- |
| **W2-PM1** | Elective | Footprinting with Multiple Kali Tools | whois, whatweb, nslookup, curl -I, wafw00f, dnsrecon / dig | `networkwalks.com` |
| **W2-PM2** | Elective | GHDB-Based Footprinting Attacks | Google Hacking Database (GHDB) operators (`intitle:`, `inurl:`, `filetype:`) | Open Web Directories & Repositories |
| **W2-PM3** | Elective | Maltego-Based Footprinting Attacks | Maltego Graph Desktop v4.14.0 (WHOIS & PGP Transforms) | `networkwalks.com` |
| **W2-PM4** | Elective | theHarvester-Based Footprinting Attacks | theHarvester v4.10.1 (`-b baidu` vs. `-b all`) | `microsoft.com` |
| **W2-PM5** | Essential | Zenmap-Based Network Scanning | Zenmap / Nmap (Ping Sweep, SYN Scan, Service/OS Detection, Topology) | Authorized Lab Network / Hosts |
| **W2-PM-FINAL** | Essential | Consolidated Technical Reporting | Reproducible Walkthroughs, Evidence Mapping & Remediation Roadmaps | All Week 2 Modules |

---

## Module-by-Module Technical Highlights

### 1. Multi-Tool Command-Line Footprinting (W2-PM1)
* **Executed:** A 6-step enumeration workflow in Kali Linux against `networkwalks.com`.
* **Key Findings:** Resolved IPv4 `192.232.216.135` (HostGator NS, GoDaddy Registrar, unsigned DNSSEC), fingerprinted Apache + WordPress stack with `HttpOnly` session cookies, enumerated MX/SPF records, and confirmed active ModSecurity (SpiderLabs) Web Application Firewall protection.

### 2. Google Hacking Database & Dorks (W2-PM2)
* **Executed:** Advanced search operator queries to locate administrative portals, configuration backups, and exposed file directories.
* **Key Findings:** Demonstrated how threat actors leverage search engine indexing to bypass direct perimeter defenses and discover sensitive exposed assets.

### 3. Graphical Link Analysis with Maltego (W2-PM3)
* **Executed:** Windows deployment of Maltego Graph Desktop v4.14.0 and execution of WHOIS and PGP server transforms on `networkwalks.com`.
* **Key Findings:** Visually mapped domain entity relationships, successfully recovering `abuse@godaddy.com` and organizational contact `info@networkwalks.com`.

### 4. Open-Source Intelligence with theHarvester (W2-PM4)
* **Executed:** Comparative OSINT extraction against `microsoft.com` using Baidu (`-b baidu -l 1000`) and multi-source aggregation (`-b all -l 50`).
* **Key Findings:** Analyzed regional search engine indexing limitations versus multi-source cloud subdomain enumeration (`*.fabric-df.microsoft.com`).

### 5. Network Discovery with Zenmap / Nmap (W2-PM5)
* **Executed:** Active network scanning utilizing ping sweeps, SYN stealth scans, and OS/service version detection scripts.
* **Key Findings:** Mapped active host topologies, open ports, and operating system fingerprints across the test environment.

---

## Repository Structure

```text
networkwalks-week2-recon-portfolio/
│
├── README.md               # Comprehensive portfolio documentation
├── reports/                # Professional Word (.docx) technical reports
│   ├── Week2_Consolidated_Footprinting_Reconnaissance_Report.docx
│   └── Maltego_Installation_and_OSINT_Walkthrough_Report.docx
└── screenshots/            # Verified terminal and GUI evidence images
    ├── Screenshot 2026-11-10 205702.jpg
    ├── Screenshot 2026-11-13 061959.jpg
    └── ...
