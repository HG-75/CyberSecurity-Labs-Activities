# 🛡️ Windows Phishing & Worm Analysis

## 🎯 Objectives

* 🔍 Investigate how threat actors gain **Initial Access** to Windows machines using exposed services and user-driven attack methods.
* 🚨 Detect **RDP brute-force attempts** and successful breaches using Windows Security Event Logs.
* 🌐 Identify attacker IP addresses, compromised accounts, and post-compromise activity through log correlation.
* 📧 Analyze phishing attack vectors including malicious binaries, double-extension files, and LNK attachments.
* 🔗 Trace malicious download and execution chains using Sysmon event logs.
* 💾 Detect USB-based malware delivery, dropped payloads, and lateral propagation via removable media.

---

## 🛠️ Tools & Resources

### 📋 Event Viewer

Primary tool used for analyzing Windows Security `.evtx` logs across all investigation scenarios.

### ⚙️ Sysmon

Provided deep visibility into:

* Process Creation
* File Creation
* Network Connections
* Malware Execution Chains

### 🗺️ MITRE ATT&CK Framework

Used to map observed attacker behavior to:

* **T1133** – External Remote Services
* **T1190** – Exploit Public-Facing Application
* **T1566** – Phishing
* **T1091** – Replication Through Removable Media

### 🖥️ Windows Security Logs

Analyzed key Event IDs to detect:

* Authentication anomalies
* Brute-force attacks
* Successful compromises

---

## 🔎 Steps Performed

### 1️⃣ RDP Brute-Force Investigation

* Opened **Security.evtx** in Event Viewer.
* Filtered for **Failed Logon Events** to identify brute-force activity.
* Applied **Logon Type filters** to isolate remote authentication attempts originating from external IP addresses.
* Identified:

  * 🎯 Most frequently targeted account
  * 🌐 Attacker's source IP address

### 2️⃣ Successful Compromise Verification

* Switched filters to **Successful Logon Events**.
* Confirmed:

  * 👤 Compromised account
  * 🔑 Logon type used for Initial Access
* Extracted the **Logon ID** from the successful RDP session.
* Correlated the Logon ID with Sysmon logs to enumerate attacker activity after access was obtained.

### 3️⃣ Threat Actor Attribution

* Examined workstation-related fields within the authentication logs.
* Retrieved the threat actor's machine hostname for additional context.

### 4️⃣ Phishing Analysis

* Executed a malicious `.com` binary to understand how attackers disguise executables as harmless files.
* Investigated malicious **LNK shortcut files** and extracted embedded PowerShell download commands.
* Reviewed phishing artifacts to identify:

  * 📄 Double-extension files
  * 🎭 Social engineering techniques
  * 🪤 Windows hidden-extension abuse

### 5️⃣ Sysmon Execution Chain Analysis

Analyzed **Phishing-Sysmon.evtx** and reconstructed the complete attack chain:

```text
Browser Download
        ↓
Archive Extraction
        ↓
Malware Execution
        ↓
Network Connection
```

* Identified the Process ID (PID) of the phishing malware.
* Traced outbound network connections.
* Determined the malicious domain contacted by the malware.

### 6️⃣ USB Worm Investigation

* Identified malware execution from a removable drive using a non-standard drive letter.
* Determined the malicious file launched by the user.
* Located the payload dropped onto disk.
* Identified the secondary USB device to which the worm propagated.

---

## 📚 Key Learnings

Initial Access is rarely a single event—it's an entire attack chain, and every stage leaves behind valuable forensic evidence.

Whether it's:

* 🚨 Hundreds of failed RDP logon attempts
* 🔗 A malicious PowerShell command hidden inside an LNK shortcut
* 💾 Malware executed from a USB drive
* 🌐 Suspicious outbound network connections

Windows Event Logs and Sysmon provide the telemetry needed to uncover the attack.

The key takeaway is understanding:

* 🔍 Which Event IDs matter
* 🔗 How to correlate events across multiple log sources
* 🧠 How attackers abuse user trust and default Windows behaviors
* 🛡️ How defenders can detect and investigate Initial Access techniques effectively

---

## 📸 Screenshots

> 📂 Please refer to the screenshots attached in this directory for supporting evidence and analysis results.
