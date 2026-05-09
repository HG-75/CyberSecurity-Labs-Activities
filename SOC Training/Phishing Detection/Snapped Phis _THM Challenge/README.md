# 🎣 Phishing Kit & Credential Harvesting Investigation Lab

## 📝 Overview

In this lab, I investigated a phishing campaign targeting employees at SwiftSpend Financial. Multiple employees received suspicious phishing emails, and some users had already submitted their credentials, resulting in account access issues. My task was to analyze the phishing emails, investigate malicious URLs, uncover the phishing kit infrastructure, and identify how the adversary collected compromised credentials.

---

## 🎯 Objectives

- 📧 Analyze phishing email samples
- 🔍 Identify malicious artifacts and indicators
- 🌐 Investigate phishing URLs and redirections
- 📂 Retrieve and analyze the phishing kit
- 🧪 Investigate the phishing archive using VirusTotal
- 🕵️ Identify exposed credential logs
- 🔐 Analyze phishing kit source files
- 🧩 Decode hidden attacker information using CyberChef

---

## 🛠️ Tools Used

- 📧 Email Viewer
- 🌐 Web Browser
- 🔎 VirusTotal
- 🍳 CyberChef
- 💻 Linux Terminal Commands
  - `sha256sum`
  - `unzip`
  - `cat`
  - `grep`

---

## 🔬 Investigation Steps

### 📩 1. Email Analysis

I reviewed the phishing emails located in the `phish-emails` folder and analyzed:
- Recipient information
- Sender email address
- Suspicious attachments
- Social engineering tactics

---

### 📎 2. Attachment Investigation

I investigated the attachment sent to Zoe Duncan and identified:
- Malicious redirection URL
- Root domain of the phishing infrastructure
- Fake login portal impersonation

---

### 🌐 3. Phishing Website Analysis

I opened the phishing attachment within the VM browser to:
- Observe redirection behavior
- Identify the impersonated company login page
- Investigate exposed directories on the server

---

### 📂 4. Phishing Kit Discovery

I navigated to the exposed `/data` directory and located the phishing kit archive.

I then:
- Downloaded the ZIP archive
- Generated the SHA256 hash
- Investigated the file on VirusTotal

#### 💻 Command Used

```bash
sha256sum filename.zip
```

---

### 🦠 5. VirusTotal Investigation

Using VirusTotal, I analyzed:
- Threat classifications
- Detection results
- Archive contents
- Number of files inside the phishing kit

---

### 🔐 6. Credential Harvesting Investigation

I navigated to:

```text
/data/Update365/
```

and reviewed the exposed log files to identify:
- Captured credentials
- Users who submitted credentials multiple times

---

### 🧾 7. Phishing Kit Source Code Analysis

After extracting the phishing kit archive, I investigated the `submit.php` file to uncover:
- Credential collection mechanisms
- Adversary-controlled email address used for receiving stolen credentials

#### 💻 Commands Used

```bash
unzip archive.zip
```

```bash
cat submit.php
```

---

### 🍳 8. Flag Decoding

I returned to the phishing URL and located the `flag.txt` file.

Using CyberChef, I decoded the hidden value to uncover the final secret.

---

## 🚨 Findings

The investigation revealed a fully operational phishing infrastructure designed to:
- 🎯 Target employees with phishing emails
- 🔐 Harvest Microsoft login credentials
- 📂 Store captured credentials in exposed directories
- 📧 Send stolen credentials directly to the attacker
- 🌐 Host publicly accessible phishing kit resources

Several operational security mistakes made by the adversary exposed critical intelligence, including:
- Exposed phishing kit archive
- Public credential log files
- Accessible source code
- Hidden encoded flag data

---

# 📸 Refer to Screenshots for Reference

Detailed screenshots of:
- Email analysis
- URL investigation
- VirusTotal results
- Exposed directories
- Credential logs
- Source code analysis
- CyberChef decoding

are included for documentation and reference purposes.

---

## 📚 Skills Gained

- 📧 Phishing Email Analysis
- 🌐 URL & Redirection Investigation
- 🔐 Credential Harvesting Analysis
- 🧪 Malware & Phishing Kit Investigation
- 🦠 VirusTotal Threat Intelligence
- 🕵️ OSINT Techniques
- 💻 Linux File & Hash Analysis
- 🍳 CyberChef Decoding
- 🔎 Web Infrastructure Investigation