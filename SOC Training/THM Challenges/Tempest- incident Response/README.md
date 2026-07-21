# 🛡️ Incident Response Investigation – Malicious Document Attack

## 📌 Overview

In this investigation, I took on the role of an **Incident Responder** to analyze a workstation compromised through a malicious document. Starting from a high-severity alert escalated by the SOC team, I reconstructed the complete attack chain by examining endpoint and network artifacts.

The objective was to identify how the attacker gained initial access, trace their activities throughout the system, uncover persistence mechanisms, detect privilege escalation attempts, and document any account manipulation performed during the intrusion.

---

## 🎯 Objectives

- Investigate a workstation compromised through a malicious document.
- Analyze endpoint and network logs to reconstruct the attack timeline.
- Identify the complete execution chain initiated by the malicious file.
- Detect post-exploitation activities, persistence mechanisms, and privilege escalation attempts.
- Document Indicators of Compromise (IoCs) and key findings throughout the investigation.

---

## 🔍 Investigation Workflow

### 📄 Initial Access

- Analyzed Sysmon logs to identify the malicious document responsible for the compromise.
- Traced the execution chain from the initial file execution to subsequent malicious processes.

### 🗂️ Artifact Preparation

- Verified the integrity of the provided forensic artifacts.
- Converted Windows Event Logs into formats suitable for efficient analysis.

### ⚙️ Process Investigation

- Examined Sysmon Event IDs to correlate process creation events.
- Followed parent-child process relationships to understand attacker activity.

### 🌐 Network Analysis

- Investigated captured network traffic using PCAP analysis tools.
- Confirmed payload downloads and Command-and-Control (C2) communications.

### 🔐 Privilege Escalation & Persistence

- Identified privilege escalation attempts performed by the attacker.
- Investigated persistence mechanisms used to maintain long-term access.

### 👤 Account Manipulation

- Reviewed system activity to detect newly created or modified user accounts.
- Documented evidence of account-related attacker actions.

---

## 🛠️ Tools Used

- 🖥️ Sysmon
- 📊 Timeline Explorer
- 🌐 Wireshark
- 📡 Brim
- 🦠 VirusTotal
- 🧪 CyberChef
- 🤖 ChatGPT

---

## 📚 Skills Practiced

- Endpoint log analysis
- Windows Event Log investigation
- Sysmon event correlation
- Network traffic analysis
- Process execution tracing
- Command-and-Control (C2) detection
- Privilege escalation analysis
- Persistence identification
- Account manipulation investigation
- Incident timeline reconstruction
- Indicator of Compromise (IoC) identification

---

## 📸 Screenshots

### Initial Access – Malicious Document

![Mal Doc](TIR_1.png)

---

### Compromised User & Host Identification

![User&Machine](TIR_2.png)

---

### Malicious Infrastructure (IP & Payload Delivery)

![Mal IP](TIR_4.png)

![Payload 1](TIR_5.png)

![Payload 2 URl](TIR_12.png)

---

### Command-and-Control Communication

![Payload 2 domain](TIR_10.png)

![Payload 2 port](TIR_11.png)

![Encoding](TIR_13.png)

---

### Reverse SOCKS Proxy Establishment

![socks](TIR_21.png)

![Tool](TIR_23.png)

---

### Privilege Escalation Activity

![Privilege](TIR_25.png)

![Tool Privilege](TIR_26.png)

---

### Account Creation & Privilege Assignment

![User Creation](TIR_30.png)

![Local](TIR_31.png)

---

### Persistence Mechanism

![Comand persistence](TIR_32.png)

---

### Result

![Result 1](Result1.png)

![Result 1.1](Result1.1.png)

![Result 2](Result2.png)

![Result 3](Result3.png)

![Result 3.1](Result3.1.png)

![Result 4](Result4.png)

![Result 4.1](Result4.1.png)

![Result 5](Result5.png)

![Result 5.1](Result5.1.png)

![Result 6](Result6.png)

![Result 6.1](Result6.1.png)

---

## 💡 Key Takeaways

- Gained practical experience investigating a complete attack lifecycle initiated by a malicious document.
- Improved my ability to correlate endpoint and network evidence during incident response.
- Learned to reconstruct attacker behavior using multiple forensic artifacts.
- Strengthened my understanding of persistence, privilege escalation, and post-exploitation techniques.
- Enhanced my documentation skills by recording findings and Indicators of Compromise (IoCs) throughout the investigation.

---

## ✅ Conclusion

This investigation provided valuable hands-on experience in incident response by following a real-world attack chain from initial compromise to post-exploitation. By correlating endpoint logs, process creation events, and network traffic, I successfully reconstructed the attack timeline and documented the attacker's techniques, persistence methods, and Indicators of Compromise.

This exercise strengthened my practical SOC and Digital Forensics skills and improved my confidence in conducting structured endpoint investigations.

---

> QXV0aG9yOiBodHRwczovL2dpdGh1Yi5jb20vSEctNzU=