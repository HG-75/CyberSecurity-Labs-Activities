# 🛡️ SOC Alert Triage & Investigation with Kibana

## 📖 Overview

In this lab, I assumed the role of a Security Operations Center (SOC) Analyst and investigated suspicious activity targeting **SomeCorp's infrastructure**. Using **Elastic Stack (Kibana)** and the **Kibana Query Language (KQL)**, I analyzed security logs, identified indicators of compromise (IOCs), and correlated events across multiple data sources to reconstruct the attacker's activity.

This investigation strengthened my practical experience in log analysis, alert triage, and incident investigation using workflows commonly employed in real-world SOC environments.

---

## 🎯 Objectives

- 🔍 Analyze security events using Kibana and KQL
- 🚨 Identify indicators of compromise (IOCs)
- 🔗 Correlate events across multiple log sources
- 🕵️ Investigate security alerts and reconstruct attacker activity
- 📊 Document evidence to support investigation findings

---

## 🛠️ Tools Used

- ⚡ Elastic Stack
- 📊 Kibana
- 🔎 Kibana Query Language (KQL)

---

## 🔬 Investigation Summary

### 🌐 1. Web Attack Investigation

- Analyzed IIS web server logs.
- Identified suspicious HTTP requests.
- Investigated web-based attack indicators.
- Correlated web activity with additional security events.

---

### 👤 2. User Account Investigation

- Examined Windows authentication logs.
- Investigated account creation and authentication activity.
- Identified suspicious user account actions.
- Correlated authentication events with attacker behavior.

---

### 💻 3. Command Execution Investigation

- Investigated Windows event logs.
- Identified suspicious command execution.
- Traced attacker actions performed on the compromised system.
- Collected evidence supporting the incident investigation.

---

## 📚 Key Learnings

- Effective alert triage requires correlating multiple log sources rather than relying on a single alert.
- Kibana Query Language (KQL) enables efficient filtering and investigation of large log datasets.
- Correlating web server logs with Windows event logs provides greater visibility into attacker activity.
- IOC identification and evidence collection are essential components of SOC investigations.
- Structured documentation improves incident response and supports future investigations.

---

## 📸 Screenshots

### Suspicious HTTP POST Requests

![post](ATE_1.png)

---

### User-Agent Responsible for the POST Requests

![User-agent](ATE_2.png)

---

### Command Execution via `errorEE.aspx`

![cmd](ATE_3.png)

---

### Unauthorized User Account Creation

![new user](ATE_7.png)

---

### Command Used to Add the User to the Remote Desktop Group

![RDP](ATE_8.png)

---

### Malicious PowerShell Command Execution

![powershell](ATE_10.png)

---

### Archive Created by the Attacker

![archeive](ATE_11.png)

---

### Result

![Result 1](Result1.png)

![Result 2](Result2.png)

![Result 3](Result3.png)

---

## 📚 Skills Gained

- 📊 Kibana Log Analysis
- 🔎 Kibana Query Language (KQL)
- 🚨 Alert Triage
- 🌐 IIS Web Log Analysis
- 🪟 Windows Event Log Investigation
- 🔗 Event Correlation
- 🕵️ IOC Identification
- 🛡️ Incident Investigation
- 📝 Security Documentation

---

## 🧩 Conclusion

This lab provided practical experience investigating security alerts using Elastic Stack and Kibana. By analyzing IIS web logs, Windows event logs, and authentication events, I reconstructed attacker activity, identified indicators of compromise, and correlated evidence across multiple log sources.

The investigation strengthened my ability to perform SOC alert triage, log analysis, event correlation, and evidence-driven incident investigations using industry-standard tools.

---

> QXV0aG9yOiBodHRwczovL2dpdGh1Yi5jb20vSEctNzU=