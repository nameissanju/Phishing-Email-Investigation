# Phishing-Email-Investigation
**Phishing Email Investigation** is a SOC-focused cybersecurity project that analyzes suspicious emails through header inspection, SPF/DKIM/DMARC validation, URL and attachment analysis, IOC extraction, and threat intelligence correlation. It maps finding to the MITRE ATT&amp;CK framework and documents incidents with professional investigation reports.

# 📌 Overview

The **Phishing Email Investigation** project is a comprehensive cybersecurity investigation framework designed to analyze suspicious emails, identify phishing indicators, and document evidence using industry-standard digital forensic and email analysis techniques. The project demonstrates a structured approach to investigating potentially malicious email messages by examining email headers, sender information, authentication mechanisms, embedded URLs, attachments, and message content to determine whether an email represents a legitimate communication or a phishing attempt.

Phishing remains one of the most common initial attack vectors used by cybercriminals to compromise organizations and individuals. Attackers frequently impersonate trusted organizations, financial institutions, government agencies, cloud service providers, and well-known companies in an attempt to steal credentials, distribute malware, or conduct financial fraud. As phishing campaigns continue to evolve, security analysts must be capable of performing detailed investigations to identify malicious indicators and support incident response activities.

This project simulates the workflow performed by **Security Operations Center (SOC) Analysts**, **Incident Responders**, **Digital Forensics Investigators**, and **Threat Analysts** during real-world phishing investigations. Rather than relying solely on automated detection tools, the investigation process focuses on manual analysis and evidence collection, enabling analysts to understand how phishing attacks operate and how to identify them accurately.

The framework follows a systematic investigation methodology that begins with collecting suspicious email samples and progresses through multiple phases of analysis, including email header examination, sender verification, SPF/DKIM/DMARC validation, IP address reputation analysis, URL inspection, domain intelligence gathering, attachment examination, malware detection, and report generation. Each phase contributes valuable evidence that helps determine the legitimacy of the email while documenting indicators of compromise (IOCs) for future threat intelligence and defensive improvements.

One of the primary objectives of this project is to demonstrate practical cybersecurity investigation skills using publicly available forensic tools, online intelligence sources, and manual analysis techniques. The project emphasizes careful evidence handling, structured documentation, and repeatable investigative procedures that align with professional security operations workflows. Every step of the investigation is designed to preserve the integrity of the evidence while providing a clear explanation of how each finding contributes to the final assessment.

Throughout the investigation process, multiple technical aspects of email communication are examined, including SMTP transmission paths, Received headers, Message-ID values, Return-Path information, Reply-To manipulation, MIME encoding, authentication records, and mail server configurations. These artifacts provide critical insight into how an email traveled across the Internet and whether any part of the message has been spoofed, altered, or intentionally crafted to deceive recipients.
 threat analysis.

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
