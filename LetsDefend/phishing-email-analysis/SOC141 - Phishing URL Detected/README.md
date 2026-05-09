# SOC141 - Phishing URL Detected

## 📌 Overview
This case involves a phishing URL detection alert triggered by outbound traffic from an internal endpoint attempting to access a known malicious domain.

The activity was identified and validated as a **True Positive**, requiring containment and escalation for further investigation.

---

## 🚨 Alert Details

- **Event ID:** 86  
- **Event Time:** Mar 22, 2021, 09:23 PM  
- **Rule Name:** SOC141 - Phishing URL Detected  
- **Severity Level:** Security Analyst  

---

## 🌐 Network Information

- **Source IP:** 172.16.17.49  
- **Hostname:** EmilyComp  
- **User:** ellie  

- **Destination IP:** 91.189.114.8  
- **Domain:** mogagrocol.ru  

- **Request URL:**  
  http://mogagrocol.ru/wp-content/plugins/akismet/fv/index.php?email=ellie@letsdefend.io  

---

## 🧪 Detection Summary

- The URL was confirmed **malicious via VirusTotal**.
- Initial connection was **allowed**, but subsequent requests were **blocked by the firewall**.
- The endpoint showed signs of **compromise**.

---

## ⚠️ Impact

- Potential credential exposure (email parameter observed).
- Possible malware delivery or command-and-control communication.
- Endpoint integrity compromised.

---

## ✅ Actions Taken

- Endpoint **contained** from the network.
- Malicious domain identified and blocked.
- Incident **escalated to L2 / Incident Response team**.

---

## 🔄 Next Steps

- Perform **EDR analysis** on the endpoint.
- Conduct **full malware scan**.
- Reset user credentials.
- Review firewall and proxy logs for additional activity.

---

## 🏁 Conclusion

This alert is confirmed as a **True Positive** phishing attempt with endpoint compromise. Immediate containment was successful, and further investigation is required to assess full impact.

---