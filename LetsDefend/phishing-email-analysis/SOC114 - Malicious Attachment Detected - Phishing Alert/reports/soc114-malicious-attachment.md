# 🔍 Detailed Investigation Report – SOC114

## 📌 Alert Overview
- **Event ID:** 45  
- **Rule:** SOC114 - Malicious Attachment Detected - Phishing Alert  
- **Date & Time:** Jan 31, 2021, 03:48 PM  
- **Severity Level:** Security Analyst  
- **Action Taken by Device:** Allowed  

This alert indicates that a phishing email containing a malicious attachment was successfully delivered to the user.

---

## 📧 Email Analysis

### Email Metadata
- **Sender:** accounting@cmail.carleton.ca  
- **Recipient:** richard@letsdefend.io  
- **SMTP IP:** 49.234.43.39  
- **Subject:** Invoice  

### Email Content
The email impersonates a legitimate invoice notification:
> "Dear customer, Your invoice for the shopping you have done is attached."

### Social Engineering Indicators
- Generic greeting ("Dear customer")
- Urgency implied through invoice context
- No personalization
- Suspicious external sender domain

### Attachment Details
- **File Name / Hash:** c9ad9506bcccfaa987ff9fc11b91698d  
- **Password:** infected (commonly used to evade email security controls)

---

## 🧪 Malware Analysis

### Detection Results
- Flagged by **36/63** security vendors on VirusTotal  
- Identified as: **Trojan – RemcosRAT**

### Malware Capabilities
RemcosRAT is a Remote Access Trojan capable of:
- Full remote control of the infected system
- Keylogging and credential theft
- Screen capture and surveillance
- File manipulation and persistence

### Exploited Vulnerability
- **CVE-2017-11882**
- Microsoft Office Memory Corruption Vulnerability
- Allows remote code execution without user interaction beyond opening the file

---

## 🌐 Network Analysis

### Observed Activity
- **Source Host:** 172.16.17.45 (RichardPRD)
- The host communicated with a known malicious domain:
  - **Domain:** andaluciabeach.net

### Malicious Payload Download
- URL: http://andaluciabeach.net/image/network.exe  
- Detection: 14/91 vendors flagged as malicious

### Command & Control (C2)
- **IP Address:** 70.38.21.234  
- Indicates active attacker communication and possible data exfiltration

---

## 🖥️ Endpoint Analysis

### Suspicious Execution
- Process observed: **JuicyPotato.exe**

### Detection
- Flagged by **57/69** vendors  
- Classified as: **HackTool.JuicyPotato**

### Significance
- JuicyPotato is a known privilege escalation exploit
- Indicates attacker attempted to gain SYSTEM-level privileges
- Confirms post-exploitation activity

---

## 🔗 Attack Chain (Kill Chain Mapping)

1. **Initial Access**  
   - Phishing email delivered with malicious attachment  

2. **Execution**  
   - User opens attachment exploiting CVE-2017-11882  

3. **Persistence & Payload Delivery**  
   - RemcosRAT installed and executed  

4. **Command & Control**  
   - Communication with C2 server (70.38.21.234)  

5. **Privilege Escalation**  
   - JuicyPotato.exe executed  

6. **Potential Impact**  
   - Full system compromise  
   - Data exfiltration  
   - Unauthorized remote access  

---

## 🚨 Impact Assessment

- Compromise of endpoint (172.16.17.45)
- Unauthorized remote access via RAT
- Elevated privileges obtained
- Risk of credential theft and lateral movement

---

## 🧾 Final Verdict
✅ **True Positive – Confirmed malicious phishing attack with successful exploitation and post-exploitation activity**

---

## 🔧 Recommended Response Actions

### Immediate Actions
- Isolate the affected endpoint from the network  
- Terminate malicious processes (RemcosRAT, JuicyPotato)  
- Block domain: andaluciabeach.net  
- Block C2 IP: 70.38.21.234  

### Remediation
- Remove malicious files and persistence mechanisms  
- Perform full antivirus and EDR scan  
- Patch vulnerability CVE-2017-11882  
- Reset credentials for affected user  

### Post-Incident اقدامات
- Review logs for lateral movement  
- Monitor network for similar indicators  
- Conduct user awareness training on phishing attacks  

---