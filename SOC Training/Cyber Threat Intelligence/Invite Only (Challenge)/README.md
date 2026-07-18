# 🕵️‍♂️ Invite Only — Threat Intelligence Challenge

## 🎯 Objectives

- 🔍 Analyze a flagged SHA256 hash to identify the file, its type, and execution lineage.

- 🔗 Trace dropped files across multiple hash pivots to map the full malware delivery chain.

- 🌐 Enrich a flagged IP to identify linked files and determine the connecting malware family.

- 📑 Correlate all indicators against an original threat intelligence report to confirm attribution.

- 🍪 Identify the phishing technique, cookie-stealing tool, and redirection platform used in the attack.

---

## 🛠️ Tools & Resources

- 🧠 **TryDetectThis 2.0:** Primary platform for hash and IP enrichment, execution parent tracing, and dropped file identification.

- 🦠 **VirusTotal:** For cross-referencing hash detections, malware family labels, and indicator relationships.

- 🌍 **Google / Open-Source Reports:** For locating the original threat intelligence report linked to the flagged indicators.

---

## 🚀 Steps Performed

1. 📥 Submitted the flagged SHA256 hash to TryDetectThis 2.0 to identify the filename and associated file type.

2. 🧬 Traced the execution parent chain of the flagged hash, recording each parent file name and hash value chronologically.

3. 📦 Identified the file dropped by the flagged hash and noted its hash for further pivoting.

4. 🔎 Researched the second execution parent hash to enumerate its four malicious dropped files in order of appearance.

5. 🌐 Enriched the flagged IP to identify files associated with it and determined the malware family linking them.

6. 📚 Used open-source search to locate the original threat intelligence report referencing all flagged indicators.

7. 🍪 Extracted from the report the cookie-stealing tool targeting Google Chrome, the phishing technique employed, and the platform used to redirect victims to malicious infrastructure.

---

## 📚 Key Learnings

Threat intelligence investigations rarely stop at a single indicator. Each hash pivot reveals new dropped files, each dropped file links back to a malware family, and each malware family connects to a documented campaign. Following the full chain, from initial hash through execution parents, dropped payloads, and IP attribution, is what separates a closed alert from actionable intelligence. Cross-referencing findings against original threat reports provides the campaign context that enrichment tools alone cannot surface.

---

## 📸 Screenshots

### File Name, Type, Execution Parent, Dropped File
#### Name
![name](Chal_1.png)

#### Type
![type](Chal_2.png)

#### Execution Parent 
![Parent](Chal_3.png)

#### Dropped File
![Dropped file](Chal_4.png)

---

### Malicious Dropped Files
![mal files](Chal_5.png)
---

### Files Related to Flagged IP
![Flagged Ip files](Chal_6.png)
---

### Tool Used to Steal Cookies
![cookies](Chal_8.png)
---

### Phishing Technique Used by Attacker
![Phishing](Chal_9.png)
---

### Platform Used
![platform](Chal_10.png)
---

###  Result
![Result 1](Result1.png)

![Result 2](Result2.png)