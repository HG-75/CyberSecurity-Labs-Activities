# 📂 File & Hash Intelligence

## 📝 Overview

In this lab, I investigated suspicious files using hash-based threat intelligence and sandbox analysis. The investigation focused on identifying malicious samples, enriching them with threat intelligence from multiple platforms, extracting behavioral indicators, and mapping observed techniques to the MITRE ATT&CK framework.

---

## 🎯 Objectives

- 🔍 Identify suspicious files using heuristic indicators
- 🔐 Generate and validate cryptographic hashes
- 🌐 Enrich samples using VirusTotal and MalwareBazaar
- 🧪 Analyze malware behavior through sandbox reports
- 🛡️ Map observed techniques to the MITRE ATT&CK framework

---

## 🛠️ Tools Used

- 🦠 VirusTotal
- 🗂️ MalwareBazaar
- 🔬 Hybrid Analysis
- 💻 TryDetectThis

---

## 🔬 Investigation Summary

### 📂 1. File Inspection

Examined suspicious files to identify:

- Double extensions
- High-entropy filenames
- Masquerading techniques
- Suspicious file paths

---

### 🔐 2. Hash Analysis

Generated SHA256 hashes for the collected samples and validated them against multiple threat intelligence platforms.

---

### 🌐 3. Threat Intelligence Investigation

Investigated the samples using:

- VirusTotal detection results
- MalwareBazaar family classification
- Threat labels
- First-seen timestamps
- Associated infrastructure

---

### 🔬 4. Sandbox Analysis

Reviewed Hybrid Analysis reports to identify:

- Process execution
- Child processes
- Behavioral indicators
- Command-line activity
- Runtime artifacts

---

### 🛡️ 5. ATT&CK Mapping

Mapped observed malware behavior to MITRE ATT&CK techniques and reviewed persistence and privilege escalation methods identified during analysis.

---

## 🚨 Findings

The investigation demonstrated how multiple threat intelligence sources can be combined to build context around suspicious files.

Evidence collected during the investigation revealed:

- 🔐 Unique SHA256 hashes identifying malicious samples
- 🦠 Malware family classifications and threat labels
- 🌐 Detection results from multiple security vendors
- 🔬 Sandbox-derived behavioral indicators
- 🧩 ATT&CK techniques associated with the observed malware
- ⚙️ Suspicious command-line execution and spawned child processes

---

# 📸 Refer to Screenshots for Reference

### Bl0gger.exe Analysis

![hash](intel_2.png)

---

### Tags Identifying Bl0gger.exe

![tags](intel_9.png)

---

### Threat Classification Label (TCL)

![TCL](intel_3.png)

---

### MITRE ATT&CK Technique for Morse-Code-Analyzer

![MITRE tech](intel_8.png)

---

### Stealth Command-Line Execution

![SCL](intel_10.png)

---

### Spawned Child Process

![New process](intel_11.png)

---

### Malware Masquerading as a Windows System File

![name of file](intel_12.png)

---

### SHA256 Hashes of Malicious Samples

![SHA256](intel_15.png)

---

### Payload.exe Analysis

![file](intel_1.png)

---

### Threat Label for Payload.exe

![label](intel_16.png)

---

### Malicious File Execution

![execution](intel_18.png)

---

### Suspicious Command Execution

![cmd](intel_19.png)

---

### Associated MITRE ATT&CK Technique

![ID](intel_20.png)

---

### Result

![Result 1](Result1.png)

![Result 2](Result2.png)

![Result 3](Result3.png)

---

## 📚 Key Learnings

- Hash intelligence enables analysts to quickly identify known malicious files.
- Threat intelligence platforms enrich investigations with reputation, malware family, and campaign information.
- Sandbox analysis provides valuable insight into runtime behavior that static analysis cannot reveal.
- Mapping malware behavior to MITRE ATT&CK improves understanding of attacker techniques.
- Combining static analysis, threat intelligence, and behavioral analysis provides a comprehensive malware triage workflow.

---

## 📚 Skills Gained

- 🔐 File Hash Analysis
- 🦠 VirusTotal Investigation
- 🗂️ MalwareBazaar Intelligence
- 🔬 Hybrid Analysis
- 🕵️ Malware Triage
- 🧩 MITRE ATT&CK Mapping
- 📊 Threat Intelligence Analysis
- 🚨 SOC Investigation Workflow

---

> QXV0aG9yOiBodHRwczovL2dpdGh1Yi5jb20vSEctNzU=