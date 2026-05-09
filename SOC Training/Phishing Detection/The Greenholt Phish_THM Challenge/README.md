# 📧 Phishing Email Investigation Lab

## 📝 Overview

In this lab, I investigated a suspicious email reported by a sales executive at Greenholt. The email raised several red flags, including a generic greeting, an unusual money transfer request, and a suspicious attachment. My goal was to analyze the email, identify important artifacts, investigate its origin, and determine whether it was part of a phishing attempt.

---

## 🎯 Objectives

- 🔍 Analyze the email headers and message source
- 📨 Identify sender and reply-to information
- 🌐 Trace the originating IP address
- 🛡️ Perform SPF and DMARC analysis
- 🧪 Investigate the attachment hash using VirusTotal
- 📂 Determine the actual file type of the attachment

---

## 🛠️ Tools Used

- 📧 Email Header Analyzer
- 🌐 WHOIS Lookup
- 🛡️ SPF Record Lookup
- 📜 DMARC Lookup
- 🔎 VirusTotal
- 💻 Linux Terminal Commands
  - `sha256sum`
  - `file`

---

## 🔬 Investigation Steps

### 📩 1. Email Inspection

I opened the provided `.eml` file and reviewed:
- Subject line
- Sender information
- Reply-To address
- Attachment details

---

### 🧾 2. Header Analysis

I analyzed the email headers to identify:
- Sender email address
- Reply-To email address
- Originating IP address
- Suspicious routing activity

---

### 🌍 3. IP Address Investigation

Using WHOIS lookup, I investigated:
- IP ownership
- Hosting provider
- Potentially suspicious infrastructure

---

### 🛡️ 4. SPF & DMARC Validation

I performed:
- SPF record lookup on the Return-Path domain
- DMARC lookup to verify email authentication policies

This helped determine whether the sender was authorized to send emails from the domain.

---

### 📎 5. Attachment Analysis

I downloaded the attachment and performed:
- SHA256 hash generation
- VirusTotal hash investigation
- File type identification

#### 💻 Commands Used

```bash
sha256sum filename
```

```bash
file filename
```

---

## 🚨 Findings

The investigation revealed several indicators commonly associated with phishing attacks, including:
- ⚠️ Suspicious sender behavior
- 💸 Unusual money transfer request
- 🔄 Mismatch between sender and reply-to addresses
- 📎 Potentially malicious attachment
- ❌ Email authentication inconsistencies

Based on the analysis, the email was identified as a phishing attempt.

---

# 📸 Refer to Screenshots for Reference

Detailed screenshots of the investigation process, command outputs, header analysis, and VirusTotal results are included for reference and documentation purposes.

---

## 📚 Skills Gained

- 📧 Email Header Analysis
- 🎣 Phishing Detection
- 🕵️ Threat Investigation
- 🛡️ SPF & DMARC Validation
- 🔐 File Hash Analysis
- 🦠 Malware Attachment Investigation
