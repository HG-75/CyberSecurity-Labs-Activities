# 🔎 Splunk - Malicious Download Investigation

## 🎯 Objectives

* Investigate suspicious process execution on a host from the HR department.
* Identify malicious activity using Windows Logs.
* Correlate process execution with network behavior to detect adversary activity.
* Understand techniques like LOLBINS for payload delivery and post-exploitation activities.

## 🛠️ Tools Used

* 📊 Splunk (SIEM solution)
* 🖥️ Windows Event Logs

## 🚀 Steps Performed

* 📋 I reviewed event logs ingested into the `win_eventlogs` index.
* 🔢 I counted the total logs for March 2022 to assess the scale of activity.
* 👤 I identified potential imposter accounts based on unusual log entries.
* 🎯 I filtered logs to focus on HR department users.
* 🖥️ I tracked the execution of scheduled tasks to pinpoint the compromised host.
* ⚙️ I investigated the usage of system processes (LOLBINs) to download payloads.
* 🌐 I extracted payload download details, including the date, file name, source site, and C2 server URL.
* 🔍 I examined downloaded files for malicious patterns.

## 📚 Key Learnings

* 📝 Event logs are crucial for tracking process execution and detecting suspicious activity.
* 🕵️ Adversaries often use legitimate system processes (LOLBINs) to evade detection.
* 🔗 Correlating user activity across network segments helps identify the source and scope of compromise.
* 🎯 Post-exploitation analysis can reveal the payload origin, file artifacts, and malicious patterns for threat hunting.

## 📸 Screenshots

### Imposter User
![Imposter](MDI_2.png)
---

### Infected User
![Infected user](MDI_4.png)
---

### Tool to download Payload
![Tool](MDI_5.png)
---

### 3rd Part Site to Access Payload
![Site](MDI_7.png)
---

### C2 Server
![C2 server](MDI_8.png)
---

### Malicious Content
![Mal Content](MDI_9.png)
---

### Infected URL
![URL Infected](MDI_10.png)
---

### Result
![Result 1](Result1.png)

![Result 1.1](Result1.1.png)

---

> QXV0aG9yOiBodHRwczovL2dpdGh1Yi5jb20vSEctNzU=
