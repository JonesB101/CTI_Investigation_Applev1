CTI Case Study: macOS "ClickFix" Phishing Infrastructure
Executive Summary
This project documents a real-time investigation into malicious infrastructure targeting macOS developers in February 2026. The investigation focuses on a typosquatted Homebrew domain (homabrews.org) used to deliver the Cuckoo Stealer malware.

Key Findings
Infrastructure: The adversary utilized a Moscow-based IP (5.255.123.244) running nginx as a front-end proxy.

Malware Delivery: The subdomain raw.homabrews.org was identified as the delivery node for malicious bash scripts.

Defense Validation: During analysis on macOS Sequoia, native OS protections successfully triggered a "Malware Detected, Paste Blocked" alert, thwarting the execution of suspected malicious strings.

Tools Used
theHarvester: Passive reconnaissance and subdomain discovery.

Nmap: Active service and OS fingerprinting.

VirusTotal/OTX API: Threat feed enrichment.
