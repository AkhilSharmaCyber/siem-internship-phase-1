# 🚨 SIEM Internship Program - Phase 1 🚨  
**Title: Building My Cyber Defense Lab**

## 🧩 Overview
Welcome to the documentation repository for Phase 1 of the SIEM Internship Program. This project simulates real-world cyber attack scenarios in a controlled lab environment and builds detection logic using Splunk SIEM. Logs were collected from both Windows and Linux machines and analyzed to create effective security alerts.

---

## 🛠 Lab Setup

- **Target OS**: Windows 10 VM
- **Attacker**: Kali Linux VM
- **SIEM**: Splunk Enterprise Free Edition
- **Log Collection**:
  - Sysmon + Winlogbeat (Windows)
  - Splunk Universal Forwarder
- **Network**: Host-only or internal NAT network for log forwarding

---

## 🔍 Detection Use Cases (MITRE Mapped)

| Scenario | Description | MITRE ATT&CK | Status |
|---------|-------------|----------------|--------|
| Brute Force + Priv Login | Multiple 4625 → 4624 | T1110 + T1078 | ✅ Working |
| After-Hours Login | Admin login outside 8 AM – 6 PM | T1078 | ✅ Working |
| RDP Lateral Movement | LogonType 10 + failed RDP | T1021.001 | ✅ Working |
| Log Tampering | `wevtutil cl Security` via Sysmon | T1562.002 | ✅ Working |
| User Account Created | Event ID 4720 + 4728 | T1136.001 | ✅ Working |

---

## 📂 Documentation

- 👉 `documentation-phase-1.pdf` contains full write-up of the lab, detections, tools, screenshots, SPLs, and answers to reflection questions.
- Each `scenario-X` folder contains:
  - `detection.md`: Structured documentation for the use case
  - `logs/`: Sample log files used for testing
  - `screenshots/`: Screenshots of Splunk queries, alerts
  - `detection-spl.spl`: Final SPL query file

---

## 🧠 Reflection

The project taught practical skills in SIEM operations, log analysis, and detection engineering. Scenarios mapped to real-world attack techniques, aligned with MITRE ATT&CK, and enforced blue team mindset development.

📌 **See `documentation-phase-1.pdf` for full Q&A reflection section.**

---

## 📎 Author

- **Name**: Akhil Sharma
- **Internship**: Srida IT Consultation Pvt. Ltd.
- **Date**: May 2025

---
