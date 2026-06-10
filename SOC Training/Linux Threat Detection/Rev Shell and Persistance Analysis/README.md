# 🛡️ Linux Intrusion Analysis Lab

## 🎯 Learning Outcomes

By completing this lab, you will:

* 🔌 Learn how **reverse shells** are used during intrusions
* ⬆️ Understand how attackers perform **privilege escalation**
* 🔁 Explore the **five most common persistence techniques**
* 📊 Uncover attacker behavior using **system log analysis**

---

## 🧪 Room Focus Areas

### 🔌 Reverse Shells

* Understanding how attackers gain remote control of a system
* Identifying reverse shell connections in logs
* Tracking outbound connections initiated by compromised hosts

---

### ⬆️ Privilege Escalation

* Detecting escalation from normal user to root
* Identifying suspicious `sudo` usage
* Monitoring abnormal command execution patterns
* Tracing privilege changes through system logs

---

### 🔁 Startup Persistence

* Attackers modifying system startup behavior
* Identifying malicious scripts added to:

  * `/etc/rc.local`
  * systemd services
  * cron startup jobs
* Ensuring malware survives reboot

---

### 👤 Account Persistence

* Creation of unauthorized users
* SSH key injection into `authorized_keys`
* Modification of existing user accounts
* Detection through authentication logs

---

### 🎯 Targeted Attack Analysis

* Full attack chain reconstruction
* Identifying attacker objectives through system behavior
* Correlating logs to understand intrusion flow

---

## 🛠️ Tools Used

### 📜 ausearch

* Used for querying **auditd logs**
* Helps track:

  * Process execution
  * File modifications
  * Privilege changes

---

### 📄 cat command

* Used for reading log files directly
* Commonly used on:

  * `auth.log`
  * `authorized_keys`
  * system configuration files

---

### 📊 Log Analysis

#### 🔐 auth.log

* Tracks authentication events
* Detects:

  * SSH brute-force attempts
  * Successful logins
  * Suspicious login patterns

#### 🔑 authorized_keys

* Used to detect SSH key-based persistence
* Helps identify unauthorized access backdoors

---

## 🔍 Key Investigation Techniques

* Correlating **auth.log + auditd logs** to trace attacker movement
* Identifying reverse shell execution patterns
* Tracking privilege escalation attempts via command history
* Detecting persistence mechanisms across system reboot cycles
* Reconstructing the full **attack timeline**

---

## 📸 Screenshots 

All evidence and investigation screenshots related to this lab are included above in the repository.

---

## 🧠 Key Takeaways

* Attackers often start with a **reverse shell** to gain control
* Privilege escalation is critical for gaining full system access
* Persistence ensures attackers maintain access even after reboot
* Logs such as `auth.log` and `auditd` are essential for forensic analysis
* Combining multiple log sources provides full attack visibility

---

## 🧩 Conclusion

This lab demonstrates how attackers maintain long-term access to Linux systems through reverse shells, privilege escalation, and persistence techniques. By analyzing system logs using tools like `ausearch` and `cat`, defenders can reconstruct the full intrusion path and identify malicious activity with precision.
