# Phishing Email Analysis (SOC Lab)

## 📌 Overview
This project demonstrates a hands-on phishing email analysis performed on a Linux virtual machine using Sublime Text and open-source threat intelligence tools.  
A spoofed phishing email sample was analyzed to identify malicious indicators and determine whether the email was a phishing attempt.

---

## 🎯 Objectives
- Analyze raw email headers to identify spoofing
- Extract and validate URLs and sender information
- Analyze attachment metadata safely
- Document Indicators of Compromise (IOCs)
- Practice SOC-style investigation and reporting

---

## 🧰 Tools Used
- Linux (Ubuntu/Kali)
- Sublime Text (email header & regex analysis)
- VirusTotal (URL & file reputation)
- urlscan.io (URL behavior analysis)
- grep & regex (IOC extraction)

---

## 🗂 Project Structure
phishing-email-analysis-lab/
├── email_samples/
├── analysis/
├── iocs/
├── screenshots/
└── notes/



---

## 🔍 Analysis Workflow

### 1️⃣ Email Header Analysis
- Examined `Received` headers to identify originating IP
- Checked SPF, DKIM, and DMARC authentication results
- Compared From and Return-Path domains for spoofing

### 2️⃣ URL Analysis
- Extracted URLs using regex in Sublime Text
- Checked domain reputation using VirusTotal and urlscan.io
- Identified typosquatting and suspicious redirects

### 3️⃣ Attachment Analysis
- Reviewed attachment metadata from headers
- Identified double file extension
- Validated file hash using VirusTotal (if available)

---

## 🚨 Indicators of Compromise (IOCs)
- Malicious IP addresses (sanitized)
- Suspicious domains and URLs
- Malicious attachment name
- Authentication failures (SPF/DKIM/DMARC)

---

## ✅ Final Verdict
Based on multiple indicators including authentication failures, malicious URLs, and attachment anomalies, the email was confirmed as a **phishing attempt**.

---

## ⚠️ Disclaimer
This project uses spoofed and sanitized phishing email samples for educational purposes only.  
No real user data or live malicious content is included.
