# Investigation Report – Phishing Mail Detected

## 1. Initial Triage

- Source: aaronluo@cmail.carleton.ca  
- Destination: mark@letsdefend.io  
- Subject: COVID19 Vaccine  
- Device Action: Blocked  

---

## 2. Email Analysis

- Email contains an attachment URL:
  https://download.cyberlearn.academy/download/download?url=https://files-ld.s3.us-east-2.amazonaws.com/72c812cf21909a48eb9cceb9e04b865d.zip  

- The attachment was analyzed using sandbox platforms:
  - Any.run → flagged as suspicious/malicious  
  - Hybrid Analysis → flagged as malicious  

- Email content and attachment behavior indicate phishing intent  

---

## 3. Log Analysis

- No additional logs associated with this activity  
- No evidence of execution or lateral movement  

---

## 4. Correlation Analysis

- Malicious attachment + phishing-themed subject  
- External sender targeting internal user  
- Matches known phishing patterns  

---

## 5. Conclusion

- Email confirmed as phishing attempt  
- Attachment identified as malicious  
- Threat was blocked before reaching the user  

---

## 6. Final Verdict

True Positive – Phishing Email (Blocked)

---

## 7. Learning Outcome

- Sandbox analysis is critical for attachment validation  
- Blocked emails still require investigation  
- Phishing emails often use trending themes (e.g., COVID19)  

---