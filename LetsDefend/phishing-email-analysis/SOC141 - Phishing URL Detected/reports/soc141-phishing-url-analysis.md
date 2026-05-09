# 🔍 SOC141 - Phishing URL Detected (Detailed Analysis)

## 📌 Alert Summary

An alert was triggered indicating that an internal endpoint attempted to access a phishing/malicious URL. The traffic originated from user **ellie** on host **EmilyComp**.

---

## 🧾 Log Analysis

- **Source IP:** 172.16.17.49  
- **Destination Domain:** mogagrocol.ru  
- **Request Type:** HTTP GET  

### Observations:
- The URL contains a suspicious query parameter:email=ellie@letsdefend.io

This suggests **data exfiltration or phishing tracking**.

- The domain structure indicates:
- Abuse of **WordPress plugin directory**
- Likely **compromised website hosting malicious script**

---

## 🦠 Threat Intelligence

- The domain **mogagrocol.ru** is flagged as malicious on **VirusTotal**.
- Likely associated with:
- Phishing campaigns
- Malware delivery
- Command & Control (C2) activity

---

## 🔐 Security Control Behavior

- First request: ✅ Allowed  
- Subsequent requests: ❌ Blocked by firewall  

### Interpretation:
- Indicates **initial exposure occurred**
- Security controls responded after detection
- Suggests possible **partial compromise**

---

## 🖥️ Endpoint Assessment

- Host: EmilyComp  
- Status: **Compromised (Suspected)**  

### Indicators:
- Access to confirmed malicious URL
- Data passed via URL parameters
- Firewall blocking after initial request

---

## ⚠️ Risk Assessment

| Risk Factor              | Level |
|--------------------------|------|
| Malware Infection        | High |
| Data Exfiltration        | Medium |
| Credential Exposure      | High |
| Lateral Movement Risk    | Medium |

---

## 🛠️ Actions Taken

- Endpoint **isolated/contained**
- Malicious domain **blocked**
- Alert validated as **True Positive**
- Escalated to **L2 / Incident Response**

---

## 🔄 Recommended Actions

### Immediate:
- Perform **EDR investigation**
- Run **full antivirus/malware scan**
- Reset user credentials (ellie)

### Further:
- Analyze:
- Process execution logs
- Network connections
- Browser history

- Check for:
- Persistence mechanisms
- Suspicious child processes

---

## 🧠 Analyst Conclusion

The alert represents a **confirmed phishing/malicious URL access**.  
Although firewall controls blocked subsequent traffic, the **initial successful connection suggests potential compromise**.

➡️ Final Verdict: **True Positive**  
➡️ Status: **Contained, Escalated for Deep Investigation**

---