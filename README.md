

# 📧 Phishing Email Investigation

> A practical cybersecurity project focused on analyzing phishing emails, identifying indicators of compromise (IOCs), examining email headers, investigating malicious URLs and attachments, and documenting findings using industry-standard incident response techniques.

![Python](https://img.shields.io/badge/Python-3.x-blue.svg)
![Cybersecurity](https://img.shields.io/badge/Cybersecurity-SOC-green)
![Email Security](https://img.shields.io/badge/Email-Security-red)
![License](https://img.shields.io/badge/License-MIT-yellow)

---

# 📖 Overview

Phishing remains one of the most common cyberattacks used to steal sensitive information, deliver malware, and compromise organizational networks. Security analysts must quickly identify malicious emails, extract evidence, determine attacker infrastructure, and provide actionable recommendations.

The **Phishing Email Investigation** project demonstrates the complete process of analyzing suspicious emails from a Security Operations Center (SOC) perspective. The investigation includes examining email headers, sender authentication records, embedded URLs, attachments, Indicators of Compromise (IOCs), and attacker techniques while documenting every finding in a professional incident report.

This repository is designed for cybersecurity students, SOC analysts, digital forensics enthusiasts, blue team professionals, and anyone looking to improve practical email investigation skills.

---

# 🎯 Objectives

The primary objectives of this project are:

- Analyze suspicious phishing emails
- Investigate email headers
- Identify spoofed sender information
- Validate SPF, DKIM, and DMARC records
- Detect malicious URLs
- Analyze suspicious attachments
- Extract Indicators of Compromise (IOCs)
- Understand attacker tactics
- Produce professional investigation reports
- Improve incident response workflow

---

# 📂 Project Structure

```
Phishing-Email-Investigation/
│
├── Samples/
│   ├── phishing-email.eml
│   ├── suspicious-email.msg
│
├── Email-Headers/
│   ├── header-analysis.md
│
├── URL-Analysis/
│   ├── urls.txt
│   ├── url-report.md
│
├── Attachment-Analysis/
│   ├── hashes.txt
│   ├── malware-analysis.md
│
├── IOC/
│   ├── indicators.csv
│
├── Reports/
│   ├── Investigation-Report.pdf
│
├── Screenshots/
│
├── README.md
└── LICENSE
```

---

# 🔍 Investigation Workflow

The investigation follows a structured SOC methodology.

## Step 1 – Collect the Email

- Obtain the suspicious email
- Preserve evidence
- Export as .eml or .msg
- Calculate hashes if required

---

## Step 2 – Analyze Email Header

Review the following fields:

- Return-Path
- From
- To
- Reply-To
- Message-ID
- Received
- Authentication Results
- MIME-Version
- X-Originating-IP

Determine:

- Original sender
- Mail server path
- IP addresses
- Spoofing attempts

---

## Step 3 – Verify Email Authentication

Check whether the email passes:

✅ SPF

Sender Policy Framework

✅ DKIM

DomainKeys Identified Mail

✅ DMARC

Domain-based Message Authentication

Failure of these mechanisms often indicates spoofing.

---

## Step 4 – Investigate Sender Domain

Perform:

- WHOIS lookup
- DNS lookup
- MX record lookup
- Reputation check
- Domain age analysis

Questions answered:

- Is the domain newly registered?
- Is the domain suspicious?
- Does it impersonate a legitimate company?

---

## Step 5 – URL Analysis

Extract every URL contained within the email.

Investigate:

- Domain reputation
- URL redirects
- IP hosting
- SSL certificate
- VirusTotal detection
- URLScan results
- Phishing indicators

Look for:

- Shortened URLs
- Misspelled domains
- Homograph attacks
- Credential harvesting pages

---

## Step 6 – Attachment Analysis

If attachments exist:

- Calculate MD5
- Calculate SHA1
- Calculate SHA256
- Determine file type
- Inspect metadata
- Perform static analysis
- Sandbox execution (if safe)

Common malicious attachment types:

- PDF
- DOCM
- XLSM
- ZIP
- RAR
- ISO
- EXE
- JS
- VBS

---

## Step 7 – IOC Extraction

Collect every Indicator of Compromise.

Examples include:

- IP addresses
- Domains
- URLs
- Email addresses
- File hashes
- Registry keys
- Filenames

Store IOCs in CSV format.

---

## Step 8 – Threat Intelligence

Cross-reference IOCs with:

- VirusTotal
- AbuseIPDB
- URLScan
- AlienVault OTX
- Cisco Talos
- Hybrid Analysis
- ANY.RUN

---

## Step 9 – Determine Attack Technique

Map attacker behavior to the MITRE ATT&CK Framework.

Possible techniques include:

- Phishing
- Spear Phishing
- Credential Harvesting
- User Execution
- Malicious Attachments
- Command and Control
- Initial Access

---

## Step 10 – Produce Investigation Report

Document:

- Executive Summary
- Timeline
- Email Details
- Header Analysis
- IOC List
- Malware Findings
- URL Findings
- Risk Assessment
- MITRE Mapping
- Recommendations

---

# 🔐 Indicators of Compromise (IOCs)

The investigation extracts valuable IOCs including:

- Sender Email
- Sender IP
- Reply-To Address
- Message-ID
- Domains
- URLs
- SHA256 Hashes
- MD5 Hashes
- File Names
- Hostnames

---

# 🛠 Tools Used

## Email Header Analysis

- MXToolbox
- Google Admin Toolbox
- Microsoft Message Header Analyzer

## URL Investigation

- VirusTotal
- URLScan.io
- Cisco Talos
- AbuseIPDB

## Malware Analysis

- Hybrid Analysis
- Any.Run
- Joe Sandbox

## Threat Intelligence

- AlienVault OTX
- VirusTotal
- OpenCTI

## DNS Investigation

- nslookup
- dig
- WHOIS

---

# ⚙ Investigation Process

```
Suspicious Email
        │
        ▼
Header Analysis
        │
        ▼
Authentication Check
        │
        ▼
Domain Investigation
        │
        ▼
URL Analysis
        │
        ▼
Attachment Analysis
        │
        ▼
IOC Extraction
        │
        ▼
Threat Intelligence
        │
        ▼
Incident Report
```

---

# 📊 Skills Demonstrated

This project demonstrates practical experience in:

- Email Security
- Phishing Detection
- Incident Response
- Digital Forensics
- Threat Intelligence
- IOC Extraction
- Malware Analysis
- DNS Investigation
- Header Analysis
- SOC Operations
- Blue Team Methodology
- MITRE ATT&CK Mapping
- Report Writing
- Cyber Threat Analysis

---

# 💼 Resume Skills

This project highlights experience in:

- Security Operations Center (SOC)
- Phishing Investigation
- Email Header Analysis
- Malware Investigation
- Threat Hunting
- Threat Intelligence
- Digital Forensics
- Network Security
- Incident Handling
- IOC Analysis
- MITRE ATT&CK
- Security Documentation

---

# 🚀 Future Improvements

Future enhancements may include:

- Automated header parser
- IOC extraction scripts
- VirusTotal API integration
- AbuseIPDB API support
- URL reputation automation
- YARA rule integration
- Sigma rule generation
- Email scoring engine
- Automated PDF report generation
- Dashboard visualization

---

# 🎓 Learning Outcomes

By completing this project, you will gain practical knowledge of:

- Phishing attack lifecycle
- Email authentication protocols
- Social engineering techniques
- IOC collection
- Threat intelligence platforms
- Malware investigation
- Digital forensics
- Security documentation
- Incident response methodology

---

# 🤝 Contributing

Contributions are welcome!

You can contribute by:

- Adding phishing samples
- Improving documentation
- Enhancing automation
- Reporting issues
- Adding threat intelligence integrations

Fork the repository and submit a Pull Request.

---

# 📜 License

This project is licensed under the MIT License.

---

# ⭐ Support

If you found this project useful:

⭐ Star the repository

🍴 Fork the project

📢 Share it with the cybersecurity community

Happy Hunting!
