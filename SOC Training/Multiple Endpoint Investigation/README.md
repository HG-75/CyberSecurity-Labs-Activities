# 🔥 Multiple Endpoints Compromise

## 🎯 Objectives

- 🖥️ Investigate the initial compromise of the CEO's workstation via a malicious ISO attachment.
- 🔍 Trace the stage 1 payload execution chain through file implantation, persistence, and C2 establishment.
- 🔐 Identify the UAC bypass technique and credential dumping tool used to escalate privileges.
- 🌐 Analyse lateral movement activity across multiple machines using harvested credentials and remote file shares.
- 💥 Uncover the final stage of the attack including domain controller compromise, DCSync, and ransomware deployment.

---

## 🛠️ Tools & Resources

- 📊 **Elastic Stack (SIEM):** Primary investigation platform for querying and correlating endpoint logs across all stages of the attack.

---

## 📋 Steps Performed

Investigated the attack campaign targeting the CEO of Quick Logistics LLC (simulated) via a phishing email with an ISO payload, covering:

- 📌 Stage 1 payload execution, identifying the initiating PID, the full command line used to implant a file to a secondary location, and the subsequent execution of the implanted file.
- ⏰ Scheduled task created by the malicious script for persistence, and the C2 IP and port established by the implanted file.
- 🛡️ UAC bypass process identified following confirmation of local administrator access, and the GitHub link used to download a credential dumping tool.
- 🔑 Username and hash of the credentials dumped from the first machine, and the remote file accessed by the attacker during share enumeration.
- 🌍 New credentials discovered from the remote file contents, the target hostname for lateral movement, and the parent process of the malicious command executed on the second compromised machine.
- 🏢 Credentials dumped from the second machine, the additional account targeted in the DCSync attack against the domain controller, and the ransomware binary download link.

---

## 📚 Key Learnings

The attack shows a fully matured threat actor operating with precision across multiple machines and privilege levels. Each phase builds on the last, credential dumping enables lateral movement, lateral movement enables domain controller access, and domain controller access enables ransomware deployment at scale. Elastic Stack correlation across endpoints is what makes this chain visible, connecting process executions on the first machine to attacker commands on the second and ultimately to the domain-level impact.

---

## 📸 Screenshots

### Stage 1 Payload, Execution, Persistance
#### Payload
![Payload 1](MEI_2.png)
---
#### Execution
![execution](MEI_3.png)
---
#### Persistence
![Persistence](MEI_4.png)
---

### C2 Connection IP & Port
#### IP
![Ip&Port](MEI_5.png)
#### Port
![Ip&Port](MEI_6.png)
---

### UAC bypass
![UAC bypass](MEI_7.png)
---

### Cred Dumping Tool
![mimikatz tool](MEI_8.png)
---

### Username & Hash of Infected User
#### Username
![Username&Hash](MEI_9.png)
#### Hash
![hash](MEI_10.png)
---

### Remote Share File Accessed
![filename](MEI_11.png)
---

### 2nd compromise Target
#### Name
![target 2](MEI_11.png)
#### Password
![target password](MEI_12.png)
---

### Lateral Movement machine name
![machine name](MEI_13.png)

![exe file](MEI_14.png)
---

### Credentials Dump in target
![cred dump](MEI_15.png)
---

### 3rd  payload 
![3rd payload](MEI_16.png)
---

### Ransomeware Link
![Ransome Link](MEI_17.png)
---

### Result
![Result 1](Result1.png)

![Result 1.1](Result1.1.png)

![Result 1.2](Result1.2.png)