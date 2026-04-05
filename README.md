<div align="center">

```
██████╗  ██████╗ ██╗  ██╗██╗████████╗    █████╗ ███████╗██╗    ██╗ █████╗ ██╗     
██╔══██╗██╔═══██╗██║  ██║██║╚══██╔══╝   ██╔══██╗██╔════╝██║    ██║██╔══██╗██║     
██████╔╝██║   ██║███████║██║   ██║      ███████║███████╗██║ █╗ ██║███████║██║     
██╔══██╗██║   ██║██╔══██║██║   ██║      ██╔══██║╚════██║██║███╗██║██╔══██║██║     
██║  ██║╚██████╔╝██║  ██║██║   ██║      ██║  ██║███████║╚███╔███╔╝██║  ██║███████╗
╚═╝  ╚═╝ ╚═════╝ ╚═╝  ╚═╝╚═╝   ╚═╝      ╚═╝  ╚═╝╚══════╝ ╚══╝╚══╝ ╚═╝  ╚═╝╚══════╝

H U N T I N G  —  D E T E C T I N G  —  R E S P O N D I N G
```

# 🛡️ SOC Analyst & Threat Hunter Portfolio

**Rohit Aswal · SOC Analyst | Threat Hunter | Digital Forensics & Incident Response**

[![Splunk](https://img.shields.io/badge/Tool-Splunk%20Enterprise-black?style=flat-square&logo=splunk&logoColor=green)](https://www.splunk.com/)
[![Wireshark](https://img.shields.io/badge/Tool-Wireshark-1679A7?style=flat-square&logo=wireshark)](https://www.wireshark.org/)
[![Python](https://img.shields.io/badge/Tool-Python-3776AB?style=flat-square&logo=python&logoColor=white)](https://www.python.org/)
[![MITRE](https://img.shields.io/badge/Framework-MITRE%20ATT%26CK-orange?style=flat-square)](https://attack.mitre.org/)
[![Kali](https://img.shields.io/badge/OS-Kali%20Linux-557C94?style=flat-square&logo=kalilinux&logoColor=white)](https://www.kali.org/)
[![CEH](https://img.shields.io/badge/Certified-CEH%20Practical-red?style=flat-square)](https://www.eccouncil.org/)

---

*Hands-on SOC investigations and security tooling — reconstructing real attack chains across DNS, HTTP, TLS, memory, and disk using Splunk SIEM, Wireshark, and Volatility. Also building ML-powered automation to make detection faster.*

</div>

---

## 👨‍💻 About Me

| | |
|---|---|
| **Name** | Rohit Aswal |
| **Role Focus** | SOC Analyst · Threat Hunter · DFIR · Detection Engineering |
| **Primary Tools** | Splunk Enterprise · Wireshark · Volatility · Python |
| **Methodology** | MITRE ATT&CK-aligned multi-layer investigation & ML-assisted triage |
| **Education** | MSc Cybersecurity, Threat Intelligence & Digital Forensics — University of Salford |
| **LinkedIn** | [![LinkedIn](https://img.shields.io/badge/-rohit--aswal08-0A66C2?style=flat-square&logo=linkedin)](https://www.linkedin.com/in/rohit-aswal08) |
| **GitHub** | [![GitHub](https://img.shields.io/badge/-rohit--aswal08-181717?style=flat-square&logo=github)](https://github.com/rohit-aswal08) |

---

## 🗂️ Portfolio Overview

```
┌─────────────────────────────────────────────────────────────────────────────────┐
│                         INVESTIGATION PORTFOLIO                                 │
├──────────────────────┬──────────────────────┬───────────────────────────────────┤
│   NETWORK & SOC      │   DIGITAL FORENSICS  │   ML & AUTOMATION                 │
│                      │                      │                                   │
│  PhantomStealer      │  Bank Fraud          │  AI SOC Alert                     │
│  DNS · HTTP · TLS    │  Disk Forensics      │  Prioritisation                   │
│                      │                      │  Framework                        │
│  BOTS v1 Attack      │  Raccoon Stealer     │                                   │
│  Investigation       │  Network Forensics   │  ~100% Real-World Acc.            │
│                      │                      │  31.3% Workload ↓                 │
│  Windows EventLog    │  Malicious PDF       │  175,341 Records · 4 Models       │
│  Threat Hunting      │  Memory Forensics    │  Benchmarked                      │
└──────────────────────┴──────────────────────┴───────────────────────────────────┘
```

---

## 🔍 Project 1 — SOC Threat Hunting: PhantomStealer Multi-Protocol C2

> **[SOC-Threat-Hunting-Portfolio](https://github.com/rohit-aswal08/SOC-Threat-Hunting-Portfolio)** · Real-world malware PCAP · Splunk SIEM · 3-part series

![DNS](https://img.shields.io/badge/Protocol-DNS-blue?style=for-the-badge)
![HTTP](https://img.shields.io/badge/Protocol-HTTP-purple?style=for-the-badge)
![TLS](https://img.shields.io/badge/Protocol-TLS%2FSSL-red?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen?style=for-the-badge)

A 3-part investigation reconstructing a complete malware attack chain from a real PCAP dataset sourced from [Malware Traffic Analysis](https://www.malware-traffic-analysis.net/). Each project targets a different protocol layer.

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                        PHANTOMSTEALER ATTACK CHAIN                          │
├─────────────────┬─────────────────┬─────────────────────────────────────────┤
│   PROJECT 1     │   PROJECT 2     │   PROJECT 3                             │
│   DNS Layer     │   HTTP Layer    │   TLS Layer                             │
│                 │                 │                                         │
│  C2 Beaconing   │  Config File    │  Encrypted C2                           │
│  Detection      │  Downloads      │  Channel Detection                      │
│                 │                 │                                         │
│  T1071.004      │  T1071.001      │  T1573                                  │
│                 │  T1105          │                                         │
└────────┬────────┴────────┬────────┴──────────┬──────────────────────────────┘
         │                 │                   │
         └────────>────────┴─────────>─────────┘
              DNS resolves    HTTP downloads      TLS encrypts
              C2 domain       config files        C2 traffic
```

### 🧠 Key Findings

| Finding | Detail | Severity |
|--------|--------|----------|
| C2 Domain (Primary) | `scxzswx.lovestoblog.com` → `185.27.134.154` | 🔴 Critical |
| C2 Domain (Secondary) | `exczx.com` → `185.38.151.11` | 🔴 Critical |
| Infected Host | `10.1.30.101` | 🔴 Critical |
| HTTP Config Downloads | `arquivo_20260129190534/545.txt` | 🔴 Critical |
| Encrypted C2 | TLS connection to `exczx.com` detected via SNI | 🔴 Critical |
| Recon Behaviour | `icanhazip.com` public IP lookup | 🟡 Suspicious |

### 🛠️ Skills Demonstrated
`SPL Query Development` · `DNS Beaconing Detection` · `HTTP Payload Analysis` · `Encrypted Traffic Analysis (SNI)` · `IOC Development` · `MITRE ATT&CK Mapping` · `Cross-Protocol Correlation`

---

## 🤖 Project 2 — AI-Driven SOC Detection & Alert Prioritisation Framework

> **[AI-SOC-Alert-Framework](https://github.com/rohit-aswal08/AI-SOC-Alert-Framework)** · Python · scikit-learn · XGBoost · Independent ML Project · Real-World Validated

![Python](https://img.shields.io/badge/Language-Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![ML](https://img.shields.io/badge/Model-Random%20Forest-green?style=for-the-badge)
![Accuracy](https://img.shields.io/badge/Real--World%20Accuracy-%7E100%25-brightgreen?style=for-the-badge)
![Validated](https://img.shields.io/badge/Validated-UNSW--NB15-purple?style=for-the-badge)
![Models](https://img.shields.io/badge/Models%20Benchmarked-4-blue?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen?style=for-the-badge)

An independently built ML pipeline combining three engineering components: SOC alert classification and prioritisation, four-model benchmark comparison for evidence-based model selection, and measurable analyst workload reduction. Validated against 175,341 real-world network records from the UNSW-NB15 benchmark dataset.

| Component | Description |
|-----------|-------------|
| 🔍 **Detection Engineering** | SOC alert classification and severity prioritisation |
| 🧪 **ML Model Benchmarking** | 4 algorithms evaluated — Random Forest selected on evidence |
| ⚡ **SOC Operations Optimisation** | Quantified reduction in analyst workload |

```
          ┌──────────────────────────┐
          │   Incoming SOC Alerts    │
          └────────────┬─────────────┘
                       │
                       ▼
          ┌──────────────────────────┐
          │ Feature Extraction Layer │
          │  (5 key security signals)│
          └────────────┬─────────────┘
                       │
                       ▼
          ┌──────────────────────────┐
          │ Random Forest Classifier │
          │ Selected after 4-model   │
          │   benchmark comparison   │
          └────────────┬─────────────┘
                       │
        ┌──────────────┼──────────────┬──────────────┐
        ▼              ▼              ▼               ▼
   🔴 Critical    🟠 High        🟡 Medium        🟢 Low
        │              │              │               │
        └──────────────┴──────────────┴───────────────┘
                                │
                                ▼
              ┌─────────────────────────────────┐
              │   Automated Response Engine     │
              │  (Remediation Recommendations)  │
              └─────────────────────────────────┘
```

### 📊 Results — Synthetic & Real-World Validation

| Metric | Synthetic Data | Real Data (UNSW-NB15) |
|--------|---------------|----------------------|
| 🎯 Model Accuracy | 97.5% | **~100%** |
| 📥 Total Alerts | 1,000 | **175,341** |
| 🤖 Auto-Handled | 425 | **54,843** |
| 👨‍💻 Needs Analyst | 575 | **120,498** |
| ⚡ Workload Reduction | 42.5% | **31.3%** |

> The lower workload reduction on real data (31.3% vs 42.5%) reflects that real-world traffic contains a higher proportion of serious threats requiring human review — the correct and expected behaviour for a production SOC triage system. Special attention was given to minimising false negatives on Critical alerts, as missed high-severity threats represent the highest operational risk in SOC environments. In SOC operations literature, reducing low-value alert volume while preserving high-severity detections is widely recognised as a key factor in improving Mean Time to Respond (MTTR) — one of the most critical KPIs in enterprise security operations.

### 🧪 Model Benchmark Summary

| Model | Synthetic Acc (%) | Real Acc (%) | Real Time (s) |
|-------|------------------|--------------|---------------|
| 🥇 Random Forest | 98.0% | **~100%** | 1.78s |
| Decision Tree | 98.0% | ~100% | 0.07s |
| XGBoost | 98.0% | 99.99% | 1.59s |
| Logistic Regression | 94.0% | 99.88% | 41.02s |

> Random Forest selected over Decision Tree due to overfitting resistance, feature importance interpretability, and industry-standard deployment across SIEM/SOAR environments. Logistic Regression eliminated due to lowest accuracy and 41-second training time at scale.

### 🛠️ Skills Demonstrated
`Machine Learning Classification` · `Evidence-Based Model Selection` · `Real-World Dataset Validation` · `Feature Engineering & Cross-Dataset Mapping` · `SOC Alert Triage Logic` · `Automated Incident Response Design` · `SIEM Integration Conceptual Design` · `Python Development` · `Security Data Analysis` · `Critical Limitation Analysis`

---

## 🔍 Project 3 — Digital Forensics Investigations (Disk · Network · Memory)

> **[digital-forensics-investigations](https://github.com/rohit-aswal08/digital-forensics-investigations)** · University of Salford — Cyber Forensics (Level 7)

![Disk](https://img.shields.io/badge/Discipline-Disk%20Forensics-blue?style=for-the-badge)
![Network](https://img.shields.io/badge/Discipline-Network%20Forensics-purple?style=for-the-badge)
![Memory](https://img.shields.io/badge/Discipline-Memory%20Forensics-red?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen?style=for-the-badge)

Three hands-on DFIR case studies mirroring real-world incident response workflows.

### 📁 Case Studies

| Case | Discipline | Key Finding | Outcome |
|------|-----------|-------------|---------|
| 🏦 Bank Fraud | Disk Forensics | Disguised executables + cracked password `langley` | $5.55M in suspicious transactions uncovered |
| 🌐 Network Malware | Network Forensics | Agent Tesla / Raccoon Stealer · C2: `45.141.59.212` | Full C2 chain mapped + DLL hash extracted |
| 📄 Malicious PDF | Memory Forensics | AcroRd32.exe PID 1752 · NTLM hashes extracted | Banking phishing URLs recovered from memory |

### 🛠️ Skills Demonstrated
`FTK Imager` · `Autopsy` · `Volatility 2.6` · `Wireshark` · `John the Ripper` · `zsteg` · `Steghide` · `hashdump` · `Evidence Imaging` · `Timeline Reconstruction` · `MITRE ATT&CK Mapping`

---

## 📊 Project 4 — Windows Event Log Threat Investigation

> **[Windows-EventLog-Threat-Investigation](https://github.com/rohit-aswal08/Windows-EventLog-Threat-Investigation)** · Splunk + Sysmon v15.15 · Personal Lab

![Splunk](https://img.shields.io/badge/Tool-Splunk%20Enterprise-black?style=for-the-badge&logo=splunk&logoColor=green)
![Sysmon](https://img.shields.io/badge/Tool-Sysmon%20v15.15-blue?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen?style=for-the-badge)

### 📋 Investigation Summary

| Field | Detail |
|-------|--------|
| Host | DEADHACK (Windows 10/11) |
| Total Events Analysed | 44,553 |
| Log Sources | Security · Sysmon/Operational · Application · System |
| Detection Queries Built | 10 validated SPL queries |
| Outcome | Clean baseline established · False positive triaged · Detection queries ready to deploy |

### 🧠 Key Findings

| Finding | Detail | Verdict |
|---------|--------|---------|
| Authentication Baseline | 227 logon events — all Logon Type 2, zero failed attempts | ✅ Benign |
| Account Enumeration (4798) | 41,966 events — traced to Windows background audit process | ✅ False Positive — suppression logic documented |
| Process Chain Analysis | 19,681 Sysmon ID 1 events — one orphaned cmd.exe flagged | 🟡 Low confidence T1055 — monitor |
| Network Connections | 2,765 outbound — all Chrome on port 443 to Google LLC IPs | ✅ Benign |

### 🛠️ Skills Demonstrated
`Windows Event Log Analysis` · `Sysmon Configuration & Deployment` · `SPL Detection Engineering` · `False Positive Triage` · `Process Chain Investigation` · `MITRE ATT&CK Mapping`

---

## 🧩 Project 5 — Full Attack Investigation: Splunk BOTS v1

> **[SOC-BOTS-v1-Attack-Investigation](https://github.com/rohit-aswal08/SOC-BOTS-v1-Attack-Investigation)** · ~33 Million Events · End-to-End SOC Simulation

![Splunk](https://img.shields.io/badge/Tool-Splunk%20BOTS%20v1-black?style=flat-square&logo=splunk&logoColor=green)
![MITRE](https://img.shields.io/badge/Framework-MITRE%20ATT%26CK-orange?style=flat-square)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen?style=flat-square)

Full end-to-end attack investigation tracing a simulated enterprise compromise from reconnaissance to data exfiltration.

```
RECONNAISSANCE      →   Joomla vulnerability scanning · Directory traversal attempts
        ↓
INITIAL ACCESS      →   Brute force login → admin/batman confirmed (HTTP 200)
        ↓
EXECUTION           →   PHP web shell uploaded: /joomla/agent.php
        ↓
PERSISTENCE         →   C2 established: 23.22.63.114 → ~194 requests · 100–400ms intervals
        ↓
POST-EXPLOITATION   →   File system enumeration via web shell
        ↓
EXFILTRATION        →   ~19.8MB data transferred to attacker IP 40.80.148.42
```

### 🛠️ Skills Demonstrated
`Threat Hunting at Scale` · `Brute Force Detection` · `Web Shell Identification` · `C2 Beaconing Analysis` · `Data Exfiltration Detection` · `Attack Timeline Reconstruction` · `MITRE ATT&CK Mapping`

---

## 🗺️ MITRE ATT&CK Coverage (Across All Projects)

| Technique ID | Technique Name | Tactic | Projects |
|-------------|---------------|--------|---------|
| [T1016](https://attack.mitre.org/techniques/T1016/) | System Network Configuration Discovery | Discovery | P1 |
| [T1027](https://attack.mitre.org/techniques/T1027/) | Obfuscated Files or Information | Defence Evasion | P3 |
| [T1055](https://attack.mitre.org/techniques/T1055/) | Process Injection | Privilege Escalation | P3, P4 |
| [T1071.001](https://attack.mitre.org/techniques/T1071/001/) | Application Layer Protocol: Web | C2 | P1, P3, P4 |
| [T1071.004](https://attack.mitre.org/techniques/T1071/004/) | Application Layer Protocol: DNS | C2 | P1 |
| [T1078](https://attack.mitre.org/techniques/T1078/) | Valid Accounts | Initial Access | P4, P5 |
| [T1087.001](https://attack.mitre.org/techniques/T1087/001/) | Local Account Discovery | Discovery | P4 |
| [T1003](https://attack.mitre.org/techniques/T1003/) | OS Credential Dumping | Credential Access | P3 |
| [T1041](https://attack.mitre.org/techniques/T1041/) | Exfiltration Over C2 Channel | Exfiltration | P3, P5 |
| [T1105](https://attack.mitre.org/techniques/T1105/) | Ingress Tool Transfer | C2 | P1 |
| [T1110](https://attack.mitre.org/techniques/T1110/) | Brute Force | Credential Access | P5 |
| [T1190](https://attack.mitre.org/techniques/T1190/) | Exploit Public-Facing Application | Initial Access | P5 |
| [T1505](https://attack.mitre.org/techniques/T1505/) | Server Software Component (Web Shell) | Persistence | P5 |
| [T1573](https://attack.mitre.org/techniques/T1573/) | Encrypted Channel | C2 | P1 |

---

## 🛠️ Full Toolkit

```
┌─────────────────────────────────────────────────────────────────────┐
│                        SOC ANALYST TOOLKIT                          │
├──────────────────┬──────────────────┬───────────────────────────────┤
│   SIEM           │   FORENSICS      │   NETWORK ANALYSIS            │
│                  │                  │                               │
│  • Splunk        │  • Autopsy       │  • Wireshark                  │
│  • SPL Queries   │  • FTK Imager    │  • PCAP filtering             │
│  • Log           │  • Volatility    │  • DNS/HTTP/TLS               │
│    Correlation   │    2/3           │    dissection                 │
│  • Alert Triage  │  • John the      │  • VirusTotal                 │
│                  │    Ripper        │  • SNI extraction             │
│                  │  • zsteg         │                               │
├──────────────────┼──────────────────┼───────────────────────────────┤
│   ML & PYTHON    │   OFFENSIVE      │   FRAMEWORKS                  │
│                  │                  │                               │
│  • scikit-learn  │  • Nmap          │  • MITRE ATT&CK               │
│  • XGBoost       │  • Metasploit    │  • NIST CSF                   │
│  • pandas        │  • Kali Linux    │  • ISO/IEC 27001              │
│  • Random Forest │  • Privilege     │                               │
│  • Jupyter       │    Escalation    │                               │
│  • UNSW-NB15     │                  │                               │
│    Validation    │                  │                               │
└──────────────────┴──────────────────┴───────────────────────────────┘
```

---

## 📊 Portfolio Skills Matrix

| Skill | P1 | P2 | P3 | P4 | P5 |
|-------|----|----|----|----|-----|
| Threat Hunting Methodology | ✅ | | ✅ | ✅ | ✅ |
| SIEM / SPL Development | ✅ | | | ✅ | ✅ |
| Network Traffic Analysis | ✅ | | ✅ | ✅ | ✅ |
| IOC Extraction & Documentation | ✅ | | ✅ | ✅ | ✅ |
| Digital Forensics (Disk/Memory) | | | ✅ | | |
| Machine Learning & Automation | | ✅ | | | |
| Real-World Dataset Validation | | ✅ | | | |
| Evidence-Based Model Selection | | ✅ | | | |
| False Positive Triage | | | | ✅ | |
| Detection Engineering | ✅ | ✅ | | ✅ | ✅ |
| MITRE ATT&CK Mapping | ✅ | | ✅ | ✅ | ✅ |
| Python & Security Scripting | | ✅ | | | |
| Attack Chain Reconstruction | ✅ | | ✅ | | ✅ |
| Professional Security Reporting | ✅ | ✅ | ✅ | ✅ | ✅ |

---

## ⚠️ Disclaimer

All investigations are performed in **controlled lab environments** using **publicly available datasets** — including [malware-traffic-analysis.net](https://www.malware-traffic-analysis.net/), the [Splunk BOTS v1 dataset](https://github.com/splunk/botsv1), and the [UNSW-NB15 benchmark dataset](https://research.unsw.edu.au/projects/unsw-nb15-dataset). Academic DFIR cases are based on simulated scenarios. No real systems were compromised. All findings are for educational and portfolio purposes only.

---

<div align="center">

**Rohit Aswal** · SOC Analyst · Threat Hunter · DFIR
*🔐 Interests: SOC Analysis · Digital Forensics · Incident Response · Threat Hunting · Security Automation*

[![LinkedIn](https://img.shields.io/badge/LinkedIn-rohit--aswal08-0A66C2?style=flat-square&logo=linkedin)](https://www.linkedin.com/in/rohit-aswal08)
[![GitHub](https://img.shields.io/badge/GitHub-rohit--aswal08-181717?style=flat-square&logo=github)](https://github.com/rohit-aswal08)

</div>
