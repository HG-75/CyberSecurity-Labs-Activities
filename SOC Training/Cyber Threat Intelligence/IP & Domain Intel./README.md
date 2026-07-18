# 🛡️ IP and Domain Threat Intelligence

This repository contains hands-on investigations focused on **IP and Domain Threat Intelligence**. The exercises demonstrate how open-source intelligence (OSINT) and infrastructure analysis can be used to enrich indicators, identify malicious activity, and provide additional context for SOC triage.

## 🎯 Objectives

- Perform IP and domain enrichment.
- Investigate WHOIS records and DNS information.
- Analyze Autonomous Systems (ASNs) and geolocation data.
- Identify exposed services and malicious infrastructure.
- Detect VPNs, proxies, and Tor exit nodes.
- Correlate intelligence from multiple sources instead of relying on a single verdict.

---

# 🌐 Domain Enrichment

Domain enrichment helps provide context around suspicious domains by examining DNS records, WHOIS information, hosting providers, and domain age.

### 🔍 Activities Performed

- Identified the IP address associated with malicious domains.
- Investigated domain creation dates.
- Determined cloud providers hosting attacker infrastructure.
- Examined CDN usage.
- Evaluated domain age at the time alerts were generated.
- Used DNS resolution and record analysis for additional context.

### 🛠️ Tools Used

- **WHOIS**
- **NSLookup**
- **VirusTotal**

---

# 🌍 IP Enrichment

IP enrichment provides valuable information about attacker infrastructure and ownership.

### 🔍 Activities Performed

- Determined IP geolocation.
- Identified Autonomous System Numbers (ASNs).
- Investigated organizations associated with malicious IPs.
- Correlated IP information with threat intelligence sources.
- Examined comments and community intelligence.

### 🛠️ Tools Used

- **VirusTotal**
- **BGP.Tools**

---

# 🚪 Service Exposure

Open services often reveal valuable information about adversary infrastructure and active command-and-control servers.

### 🔍 Activities Performed

- Enumerated exposed services.
- Identified open ports.
- Investigated remote access protocols.
- Detected active Command-and-Control (C2) servers.
- Examined SSL/TLS certificates.
- Determined the operating system of attack servers.

### 🛠️ Tools Used

- **Censys**
- **VirusTotal**

---

# 🔐 VPN Detection

VPN and proxy detection provide additional context during investigations and help distinguish legitimate users from suspicious infrastructure.

### 🔍 Activities Performed

- Identified VPN infrastructure.
- Detected proxy and anonymity services.
- Investigated Tor-related indicators.
- Correlated infrastructure with reputation sources.

### 🛠️ Tools Used

- **VirusTotal**
- **BGP.Tools**

---

# 🧰 Tools Utilized

| Tool | Purpose |
|--------|---------|
| 🦠 VirusTotal | Threat intelligence and reputation analysis |
| 🌐 WHOIS | Domain registration information |
| 📡 NSLookup | DNS resolution and record analysis |
| 🔎 Censys | Internet-facing service enumeration |
| 🛣️ BGP.Tools | ASN and network intelligence |

---

# 📚 Skills Demonstrated

- Threat Intelligence
- Indicator Enrichment
- OSINT Analysis
- Domain Investigation
- IP Investigation
- Service Enumeration
- Infrastructure Attribution
- VPN and Proxy Detection
- SOC Triage
- Threat Correlation

---

# 📸 Screenshots

## IP (2.58.56.60)
---
### Country it based in
![country](intel_3.png)
---

### C2 server hosting ip
![C2](intel_4.png)
---

### Autonomous System it belongs
![ASN](intel_5.png)
---

### Tags attributed to ASN
![tags](intel_6.png)
---

## IP (64.89.160.44)
---
### Service exposed
![service](intel_7.png)
---

### Ports Open
![port](intel_8.png)
---

### port which leaks C2 server
![C2 server](intel_9.png)
---

## IP (35.188.105.97)

![Ipaddress](intel_11.png)
---

### Cloud Server 
![Cloud](intel_12.png)
---

### Country hosting malicious server
![mal country](intel_13.png)
---

### Attacker's Server OS
![Server OS](intel_15.png)
---

### Result
![Result 1](Result1.png)

![Result 2](Result2.png)

![Result 3](Result3.png)

![Result 4](Result4.png)
