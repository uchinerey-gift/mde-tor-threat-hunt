# 🕵🏾‍♀️ Microsoft Defender Advanced Hunting — Unauthorized TOR Usage Lab

![TOR Threat Hunt Complete](https://img.shields.io/badge/TOR%20Threat%20Hunt-Complete-brightgreen)
![Platform](https://img.shields.io/badge/Platform-Microsoft%20Defender-blue)
![Tools](https://img.shields.io/badge/Tools-KQL%20%7C%20PowerShell-orange)
![Focus](https://img.shields.io/badge/Focus-Threat%20Hunting%20%7C%20EDR-lightgrey)

A hands-on Microsoft Defender for Endpoint threat-hunting project demonstrating how unauthorized TOR Browser activity appears across file, process, and network telemetry — and how to investigate it using Advanced Hunting (KQL).

---

## 📌 Project Overview

This lab simulates a realistic enterprise security scenario in which a user downloads, silently installs, launches, and uses the TOR Browser on a managed Windows endpoint. Additional suspicious behavior is introduced through basic anti-forensics techniques.

The project demonstrates how a SOC analyst validates endpoint visibility, identifies unauthorized anonymization tools, correlates telemetry across multiple data sources, and documents findings in a clear, professional format suitable for escalation or reporting.

A full HTML case study is included to showcase investigation methodology, evidence handling, and presentation skills beyond a traditional README.

---

## 🎯 Hunt Objectives

- Detect unauthorized TOR Browser installation and execution  
- Identify TOR-related anonymized network traffic  
- Validate Microsoft Defender for Endpoint telemetry ingestion  
- Demonstrate structured threat hunting using KQL  
- Produce portfolio-quality SOC investigation documentation  

---

## 🧰 Environment

- **Endpoint:** Windows 11 Virtual Machine (`chi-chi-vm`)  
- **Security Platform:** Microsoft Defender for Endpoint  
- **Hunting Interface:** Microsoft Defender Advanced Hunting  
- **Languages & Tools:** PowerShell, KQL  
- **Key Tables Used:**  
  - `DeviceInfo`  
  - `DeviceFileEvents`  
  - `DeviceProcessEvents`  
  - `DeviceNetworkEvents`  

---

## 🔍 Investigation Summary

The following activity was simulated and successfully identified using Microsoft Defender telemetry:

- TOR installer downloaded to the endpoint  
- Silent TOR installation executed  
- TOR Browser launched  
- Anonymized TOR network traffic generated  
- Suspicious file created, modified, and deleted to simulate anti-forensics behavior  

Each action was validated through Advanced Hunting queries and documented with supporting evidence.

---

## 🧪 Investigation Walkthrough

A full step-by-step investigation is documented in the interactive HTML case study:

👉 **Open `index.html` in a browser to view the complete investigation**

The report includes:
- Clearly defined investigation phases  
- PowerShell commands used to generate activity  
- Evidence screenshots  
- KQL queries per activity type  
- KQL results screenshots  
- Analyst-style narrative and findings  

---

## 🧠 Skills Demonstrated

- Threat hunting using **Microsoft Defender for Endpoint (Advanced Hunting)**  
- Writing and refining **Kusto Query Language (KQL)** queries  
- Correlating **file, process, and network** telemetry  
- Detecting **unauthorized anonymization tools (TOR Browser)**  
- Validating **endpoint visibility and sensor health**  
- Identifying **basic anti-forensics behaviors** (file creation, modification, deletion)  
- Producing **SOC-style investigation documentation and evidence**  

---

## 🔎 SOC & Detection Relevance

This project reflects real-world SOC workflows by demonstrating how analysts validate telemetry ingestion, identify policy-violating software without relying solely on alerts, and correlate endpoint data across multiple sources. The investigation aligns with Tier 1–2 SOC responsibilities, including initial triage, investigation, evidence collection, and clear documentation for escalation or compliance review.

---

## 📈 Continuous Development

This project represents an ongoing focus on strengthening SOC analyst skills through hands-on threat hunting, iterative query refinement, and professional documentation of endpoint investigations using Microsoft Defender for Endpoint.

---

## 👤 Author

**Chinerey “Chi Chi” Ukwu**  
Cybersecurity Analyst | Threat Hunting | Endpoint Security  
GitHub: https://github.com/uchinerey-gift

---

## ⚠️ Disclaimer

This project is intended for **educational and portfolio demonstration purposes only**. All activity was performed in a controlled lab environment. No real malicious activity or unauthorized access was conducted.
