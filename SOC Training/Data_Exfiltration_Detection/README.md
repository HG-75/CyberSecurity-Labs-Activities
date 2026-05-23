🔐 Data Exfiltration Detection Lab (Splunk + Wireshark)
👨‍💻 Overview

In this lab, I worked on detecting different types of data exfiltration techniques using Splunk and Wireshark.
The goal was to analyze network traffic and identify suspicious behavior across multiple protocols commonly used by attackers.

I performed all analysis from my perspective as a SOC analyst, focusing on detecting abnormal patterns and possible data leaks.

🧪 Detection Tasks
🌐 1. DNS Data Exfiltration

I analyzed DNS traffic to detect hidden or encoded data being transferred through DNS queries.

Looked for unusually long subdomains
Detected encoded patterns in DNS requests
Identified abnormal query frequency
📁 2. FTP Data Exfiltration

I inspected FTP traffic to detect unauthorized file transfers.

Monitored login attempts and credentials
Checked file upload/download activity (STOR / RETR commands)
Identified suspicious file movement over plaintext FTP
🌍 3. HTTP Data Exfiltration

I analyzed HTTP traffic for hidden data being sent over web requests.

Inspected HTTP POST requests
Identified large or encoded payloads
Detected unusual endpoints receiving data
📡 4. ICMP Data Exfiltration

I reviewed ICMP traffic to detect covert data hiding inside ping packets.

Found oversized ICMP packets
Checked payload data inside echo requests
Flagged abnormal ICMP usage patterns
📊 Tools Used
🧰 Splunk (log analysis & searching)
📡 Wireshark (packet inspection & filtering)
🖼️ Screenshots

📌 Refer to the screenshots folder for lab work proof and detailed analysis outputs.
Each detection case is supported with relevant captured evidence from Splunk and Wireshark.

🎯 Outcome

Through this lab, I improved my understanding of:

Different data exfiltration techniques
How attackers misuse common protocols
Practical detection using SIEM and packet analysis tools