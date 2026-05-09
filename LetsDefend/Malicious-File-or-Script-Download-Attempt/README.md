# SOC137 - Malicious File/Script Download Attempt

## 📌 Alert Overview
- **Event ID:** 76  
- **Event Time:** Mar 14, 2021, 07:15 PM  
- **Rule Name:** SOC137 - Malicious File/Script Download Attempt  
- **Severity Level:** Security Analyst  

## 🖥️ Affected System
- **Source IP:** 172.16.17.37  
- **Hostname:** NicolasPRD  

## 📁 File Details
- **File Name:** INVOICE PACKAGE LINK TO DOWNLOAD.docm  
- **File Hash (MD5):** f2d0c66b801244c059f636d08a474079  
- **File Size:** 16.66 KB  
- **Action Taken:** Blocked  

## 🔗 Sample File
- Password-protected sample (password: `infected`):  
  https://files-ld.s3.us-east-2.amazonaws.com/f2d0c66b801244c059f636d08a474079.zip  

## ⚠️ Threat Summary
The detected file is a malicious macro-enabled document (.docm) commonly used to deliver malware via phishing campaigns. The file was successfully blocked before execution.

## 🧾 Final Verdict
✅ **True Positive**  
The file is confirmed malicious and associated with trojan activity.

## 🔐 Recommendations
- Keep macro execution disabled by default.
- Educate users about phishing attachments.
- Ensure endpoint protection signatures are updated.
- Monitor for similar file hashes or filenames.