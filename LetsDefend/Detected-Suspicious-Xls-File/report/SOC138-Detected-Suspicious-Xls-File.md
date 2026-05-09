# Investigation Report - SOC138 Suspicious XLS File

## 1. Alert Trigger
An alert (Event ID: 77) was triggered indicating the execution of a suspicious Excel macro-enabled file on endpoint Sofia (172.16.17.56).

## 2. Initial Findings
- The file `ORDER SHEET & SPEC.xlsm` was executed by the user.
- The file was allowed by the system at the time of execution.
- Macro-enabled Excel files are commonly used to deliver malware.

## 3. File Hash Analysis
- **Hash:** 7ccf88c0bbe3b29bf19d877c4596a8d4  
- **VirusTotal Detection:** 45/64 vendors flagged as malicious  
- **Threat Label:** Trojan.acao/docdl  

This confirms the file is highly suspicious and widely recognized as malicious.

## 4. Network Activity Analysis
- The infected host initiated multiple HTTP requests to:
  - **Malicious IP:** 177.53.143.89  
- The communication occurred immediately after file execution.
- This behavior is consistent with Command and Control (C2) communication.

## 5. Endpoint Analysis
- Host Sofia (172.16.17.56) showed signs of compromise.
- The system was successfully contained to prevent lateral movement.
- No additional suspicious processes were reported beyond initial execution.

## 6. Attack Flow
1. User executed malicious Excel file  
2. Macro payload triggered  
3. Outbound connection to C2 server established  
4. System compromise confirmed  

## 7. Conclusion
The alert represents a **True Positive**. The Excel file was malicious and led to active communication with a known malicious IP, confirming compromise.

## 8. Mitigation Steps
- Isolated affected endpoint
- Blocked malicious IP (177.53.143.89)
- Added file hash to blocklist
- Recommended macro restrictions in Office applications

## 9. Recommendations
- Enforce email attachment scanning
- Disable macros unless explicitly needed
- Deploy endpoint detection and response (EDR)
- Conduct phishing awareness training for users