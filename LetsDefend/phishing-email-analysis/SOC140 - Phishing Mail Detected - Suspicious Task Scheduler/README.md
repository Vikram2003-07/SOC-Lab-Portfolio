# Phishing Mail Detected – Suspicious Task Scheduler (True Positive)

## Alert Overview

- Event ID: 82  
- Rule: SOC140 - Phishing Mail Detected - Suspicious Task Scheduler  
- Source Email: aaronluo@cmail.carleton.ca  
- Destination Email: mark@letsdefend.io  
- Subject: COVID19 Vaccine  
- SMTP Address: 189.162.189.159  
- Device Action: Blocked  

---

## Summary

An alert was triggered for a suspected phishing email containing a malicious attachment. The email was analyzed and confirmed as a phishing attempt based on attachment analysis and threat intelligence.

---

## Key Findings

- Email contains a suspicious attachment URL  
- Attachment flagged as malicious by:
  - Any.run  
  - Hybrid Analysis  
- Email characteristics align with phishing activity  
- Email delivery was blocked successfully  

---

## Impact Assessment

- No user interaction occurred  
- No execution of malicious payload  
- Threat contained at email gateway level  

---

## Final Verdict

True Positive – Phishing Email with Malicious Attachment

---

## Tools Used

- LetsDefend SIEM  
- Any.run  
- Hybrid Analysis  

---

## Evidence

Screenshots of:
- Email details  
- Attachment analysis (Any.run / Hybrid Analysis)  
- Alert details  

---