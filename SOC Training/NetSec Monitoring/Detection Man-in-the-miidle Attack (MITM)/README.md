# 🛡️ Man-in-the-Middle (MITM) Attack Analysis Lab

## 📖 Overview

In this lab, I performed network traffic analysis to detect and investigate different Man-in-the-Middle (MITM) attack techniques using Wireshark.

The objective of this room was to understand how attackers intercept network communication and how these attacks can be identified through packet analysis and network investigation techniques.

During this lab, I successfully detected:
- 🧪 ARP Spoofing
- 🌐 DNS Spoofing
- 🔓 SSL Stripping

---

# 🔍 Task 1 — Detecting ARP Spoofing

In this task, I analyzed ARP traffic to identify signs of ARP cache poisoning attacks.

## 🛠 What I Investigated
- Duplicate MAC addresses mapped to different IP addresses
- Suspicious ARP reply packets
- Abnormal ARP activity inside the network

## 📌 Detection Method
I inspected ARP traffic in Wireshark and verified ARP cache entries using:

```bash
arp -a
```

By analyzing the packets, I identified suspicious ARP responses indicating that an attacker was attempting to redirect network traffic through their machine.

## 🧠 Key Learning
ARP spoofing works by poisoning a victim’s ARP cache, allowing the attacker to position themselves between communicating devices.

---

# 🌐 Task 2 — Unmasking DNS Spoofing

In this task, I investigated manipulated DNS responses to uncover DNS spoofing activity.

## 🛠 What I Investigated
- Multiple DNS responses for the same query
- Conflicting IP address resolutions
- Suspicious DNS reply packets

## 📌 Detection Method
Using Wireshark, I filtered DNS traffic and compared legitimate responses with spoofed responses to identify abnormal behavior.

## 🧠 Key Learning
DNS spoofing tricks users into connecting to malicious servers by sending fake DNS responses before legitimate ones arrive.

---

# 🔓 Task 3 — Spotting SSL Stripping in Action

In this task, I analyzed how attackers downgrade secure HTTPS communication into insecure HTTP traffic.

## 🛠 What I Investigated
- Plaintext HTTP traffic
- Credentials transmitted without encryption
- Missing HTTPS connections

## 📌 Detection Method
I filtered HTTP traffic in Wireshark and inspected packets carrying sensitive information such as usernames and passwords in plaintext.

## 🧠 Key Learning
SSL stripping removes encryption protection between the victim and the target website, allowing attackers to intercept sensitive data.

---

# 🧠 Key Concepts Covered

## 🧩 ARP Spoofing
Detected by identifying duplicate MAC addresses and suspicious ARP replies inside the ARP cache and packet captures.

## 🌐 DNS Spoofing
Unmasked by observing multiple conflicting DNS responses for the same domain request.

## 🔓 SSL Stripping
Exposed by discovering sensitive information being transmitted in plaintext over HTTP instead of HTTPS.

---

# 🛠 Tools Used

- 🦈 Wireshark
- 💻 Linux Terminal
- 🌐 Network Protocol Analysis

---

# 📸 Refer to Screenshots

The screenshots folder contains evidence and analysis related to:
- ARP spoofing detection
- DNS spoofing investigation
- SSL stripping analysis
- Packet inspection results
- Plaintext credential capture
- Wireshark filters used during analysis

---

# 🎯 Skills Gained

- Packet analysis using Wireshark
- MITM attack detection
- ARP traffic investigation
- DNS traffic analysis
- HTTP/HTTPS inspection
- Threat hunting through network traffic
- Identifying suspicious network behavior

---

# ✅ Conclusion

This lab helped me gain practical experience in detecting and analyzing Man-in-the-Middle attacks using Wireshark. It improved my understanding of how attackers manipulate network communication and how packet analysis can be used to identify malicious activity inside a network.