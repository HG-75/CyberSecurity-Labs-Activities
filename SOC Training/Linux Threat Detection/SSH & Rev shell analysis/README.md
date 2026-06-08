# 🔐 SSH Compromise & Reverse Shell Analysis

## 🎯 Objectives

- 🔎 Detect SSH brute-force attempts and successful breaches via authentication logs.
- 🌐 Analyze web server logs to identify command injection exploitation against a vulnerable web application.
- 🌳 Build process trees using `auditd` to trace the origin of suspicious commands back to the breaching service.
- 🧠 Investigate advanced Initial Access scenarios including supply chain compromise and human-driven attacks.
- 🔁 Apply process tree analysis as a universal detection method across all Initial Access techniques.

---

## 🛠️ Tools & Resources

- 📄 **auth.log** → Detect SSH brute-force attempts, successful logins, and attacker IPs.
- 🌍 **Nginx Access Log** → Identify command injection patterns in HTTP requests.
- 🧩 **auditd** → Runtime process monitoring to build process trees using PID & PPID correlation.

---

## 🧪 Steps Performed

### 🔐 1. SSH Authentication Analysis
- Reviewed `auth.log` to determine the first SSH login of the `ubuntu` user.
- Confirmed authentication method used during access.

### 🚨 2. Brute-force Detection
- Filtered failed SSH login attempts.
- Identified:
  - ⏱️ Brute-force start time
  - 👤 Targeted usernames
  - 🌐 IP address that successfully accessed root

### 🌐 3. Web Exploitation Analysis
- Analyzed Nginx access logs.
- Detected:
  - Attacker IP
  - Vulnerable endpoint
  - 💉 Command injection payloads inside request parameters

### 📂 4. File Access via Injection
- Identified Python file accessed through injection.
- Extracted hidden flag from the file.

### 🧩 5. Process Tree Reconstruction (auditd)
- Traced `whoami` execution back to origin using PPID chain.

### 🕵️ 6. Full Attack Chain Analysis
- Enumerated child processes of compromised application.
- Identified reverse shell execution and attacker activity.

---

## 🌳 Process Tree
1 (systemd)
└── 577 (Python script)
└── 1018 (Reverse shell established)
└── 1020 (First command by attacker)

---

## 📚 Key Learnings

- ⚡ Linux Initial Access varies, but detection methodology remains consistent.
- 🧭 Process tree analysis connects malicious actions back to the original entry point.
- 📊 Application logs help narrow scope, but `auditd` provides deep runtime visibility.
- 🧠 Combining logs = full attack reconstruction with high accuracy.

---

## 🖼️ Screenshots

📁 Please refer to the attached screenshots in this directory.

---