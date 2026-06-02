# 🛡️ Detecting Web DDoS Attacks using Splunk

## 👨‍💻 About This Project

I worked on this project to understand and detect **Web DDoS (Distributed Denial of Service) attacks** using **Splunk** by analyzing real-time and historical logs.  

My main focus was to learn how attackers exploit web systems and how defenders can identify and mitigate such attacks using security tools and best practices.

---

## 🧰 Tools & Technologies Used

- 🔍 **Splunk** – For log analysis and detection
- 🌐 Web Server Logs – For monitoring incoming traffic patterns
- 📊 Dashboard Analysis – For visualizing traffic spikes and anomalies
- 🖥️ Linux Environment – For running and testing logs

---

## 🎯 Objective

The goal of this task was to:

- Detect abnormal traffic patterns 🚨  
- Identify possible DDoS behavior 💥  
- Analyze logs using Splunk 📈  
- Understand how attackers overwhelm web applications 🌍  
- Learn defensive strategies used in real-world systems 🛡️  

---

## ⚔️ What I Learned (Attack vs Defense)

Attackers constantly search for weak points to exploit, but defenders use multiple layers of protection to keep systems stable.

### 🧱 Application-Level Defense

#### 🔐 Secure Development Practices
I learned that secure coding is the first line of defense.  
Input validation plays a key role in preventing abuse of search fields and forms.

---

#### 🤖 Challenges (CAPTCHA & JS Checks)
- CAPTCHA helps verify human users 👤  
- JavaScript challenges help detect bots 🤖  
- These methods slow down or block automated attacks

---

### 🌐 Network & Infrastructure Defense

#### 🚀 Content Delivery Network (CDN)
- CDNs distribute traffic across global edge servers 🌍  
- Reduce load on origin servers  
- Help absorb DDoS traffic spikes 📉  
- Provide caching and load balancing

---

#### 🧯 Web Application Firewall (WAF)
- Filters and monitors HTTP requests 🔥  
- Blocks or challenges suspicious traffic  
- Rate limiting helps prevent abuse (e.g., /login flooding)

---

### 🌍 Large-Scale Mitigation

Modern providers like Cloudflare and Google can absorb massive attacks using global infrastructure.

- Billions of requests per second can be handled ⚡  
- Traffic is distributed and filtered intelligently  
- Attacks are mitigated before reaching origin servers 🛡️  

---

### 🧨 Attack Bypass Techniques (What I Learned)

Attackers may try to bypass defenses using:
- Random query parameters (`/page?id=1234`) 🔀  
- Changing user agents 🕵️  
- Spoofing referrers 🔗  
- Distributed geographic traffic 🌐  

---

---

 ## 📸 Screenshots

All relevant screenshots from Splunk dashboards, log analysis, and detected traffic patterns are included in the repository.

---

## 📊 Splunk Role in This Project

Using Splunk, I was able to:

- 📥 Ingest and analyze web server logs  
- 📈 Identify traffic spikes and anomalies  
- 🔍 Filter suspicious IP behavior  
- 🚨 Detect patterns consistent with DDoS attempts  
- 📊 Build insights from log data for better understanding  

---

## 🧠 Key Takeaways

- DDoS attacks are about overwhelming resources, not breaking code 💥  
- Defense requires multiple layers (App + Network + Infrastructure) 🛡️  
- Splunk is powerful for real-time log analysis and detection 📊  
- CDNs and WAFs are essential in modern web security 🌍  

---

## 🚀 Conclusion

This project helped me understand how real-world DDoS detection works and how security tools like Splunk can be used to analyze and defend against such attacks.

I now have a better understanding of both:
- ⚔️ How attacks work  
- 🛡️ How defenses are implemented in production systems  

---

## 📌 Status

✔️ Completed DDoS detection analysis using Splunk  
✔️ Gained practical understanding of mitigation techniques  
✔️ Improved log analysis and security awareness  

---