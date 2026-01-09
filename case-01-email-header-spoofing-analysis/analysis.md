# Case 01 – Email Header Spoofing Analysis

## Scenario Overview
This case involves the analysis of a spoofed phishing email provided for training purposes.  
The objective was to examine raw email headers to identify signs of sender spoofing and authentication failures commonly associated with phishing attacks.

---

## Tools Used
- Linux (Ubuntu/Kali VM)
- Sublime Text (manual header inspection & regex search)
- grep / regex (IOC extraction)
- VirusTotal (IP and domain reputation – external validation)

---

## Email Header Analysis

### 1. Received Header Inspection
The `Received` headers were reviewed from bottom to top to identify the originating mail server.

**Findings:**
- Originating IP identified from the earliest `Received` entry
- Mail server hostname did not match the claimed sender domain
- Use of generic or suspicious mail relay infrastructure

This indicates a high likelihood of email spoofing.

---

### 2. Sender Authentication Checks (SPF, DKIM, DMARC)

Authentication results extracted from the headers:

- **SPF:** Fail  
- **DKIM:** Fail  
- **DMARC:** Fail  

**Impact:**
Multiple authentication failures strongly suggest that the email was not sent from an authorized mail server and is likely spoofed.

---

### 3. From vs Return-Path Analysis
The `From` address and `Return-Path` were compared.

**Observation:**
- The visible sender domain differed from the return-path domain
- This mismatch is a common phishing technique used to bypass basic user insp
