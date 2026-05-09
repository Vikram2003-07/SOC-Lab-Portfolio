# 📧 SOC114 – Malicious Attachment Detected (Phishing Alert)

## 📌 Overview
This alert involves a phishing email delivering a malicious attachment identified as **RemcosRAT**, exploiting a Microsoft Office vulnerability (CVE-2017-11882).

## 🧪 Scenario Details
- **Event ID:** 45  
- **Alert Rule:** SOC114 - Malicious Attachment Detected  
- **Date:** Jan 31, 2021  
- **Recipient:** richard@letsdefend.io  
- **Subject:** Invoice  

## 📎 Key Indicators
- Malicious Attachment Hash: `c9ad9506bcccfaa987ff9fc11b91698d`
- Malware: RemcosRAT
- Exploit: CVE-2017-11882
- Malicious Domain: andaluciabeach.net
- C2 IP: 70.38.21.234
- Suspicious Tool: JuicyPotato.exe

## 🚨 Impact
- Remote Access Trojan execution
- Privilege escalation activity
- Potential full system compromise

## ✅ Verdict
**True Positive**

## 🔧 Response Actions
- Isolate affected system
- Block malicious domain & IP
- Remove malware & persistence
- Reset user credentials
- Patch vulnerable software