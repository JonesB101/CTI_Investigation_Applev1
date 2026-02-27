# CTI Investigation: macOS "ClickFix" Phishing Campaign
**Date:** February 2026  
**Analyst:** Brandon Jones  
**Focus:** Infrastructure Mapping & macOS Malware Delivery

## 1. Executive Summary
This report details an investigation into the **ClickFix** social engineering campaign targeting macOS users via typosquatted domains. By mimicking legitimate tools like Homebrew, the adversary attempts to deliver the **Cuckoo Stealer** infostealer. This project validates current macOS Sequoia security telemetry and maps active adversary infrastructure.

## 2. Methodology
- **Passive Reconnaissance:** Utilized `theHarvester` with VirusTotal and AlienVault OTX APIs for subdomain and IP discovery.
- **Active Reconnaissance:** Performed `nmap` service discovery and OS fingerprinting on identified delivery nodes.
- **Validation:** Analyzed native macOS Sequoia clipboard protections during interaction with malicious command strings.

## 3. Technical Findings
| Attribute | Value |
| :--- | :--- |
| **Primary Domain** | `homabrews.org` |
| **Payload Subdomain** | `raw.homabrews.org` |
| **Hosting IP** | `5.255.123.244` |
| **Service (Port 443)** | nginx (Reverse Proxy) |

## 4. Operational Observations
During the investigation, macOS Sequoia's native security features successfully intercepted a paste event containing malicious strings associated with this campaign. This validates the effectiveness of Apple's latest XProtect signatures against 2026 infostealer variants.

---
*This project was completed as part of a professional development portfolio in Information Systems and Cybersecurity.*
