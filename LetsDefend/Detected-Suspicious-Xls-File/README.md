# SOC138 - Suspicious XLS File Detection

## Overview
This case involves the detection of a suspicious Excel macro-enabled file (`.xlsm`) executed on an endpoint. The activity triggered a SOC alert due to potential malicious behavior.

## Alert Details
- **Event ID:** 77  
- **Rule:** SOC138 - Detected Suspicious Xls File  
- **Severity:** Security Analyst  
- **Timestamp:** Mar 13, 2021, 08:20 PM  

## Affected Host
- **Hostname:** Sofia  
- **IP Address:** 172.16.17.56  

## File Information
- **File Name:** ORDER SHEET & SPEC.xlsm  
- **File Hash:** 7ccf88c0bbe3b29bf19d877c4596a8d4  
- **File Size:** 2.66 MB  
- **Device Action:** Allowed  

## Summary
A macro-enabled Excel file was executed on the host Sofia. The file exhibited malicious behavior, including initiating outbound communication to a known malicious IP address.

## Verdict
**True Positive** – Confirmed malicious document leading to system compromise.

## Actions Taken
- Endpoint containment performed
- Malicious file analyzed and confirmed
- Network communication reviewed

## Recommendation
- Block malicious IP and hash across the network
- Disable macros by default in Office applications
- Conduct user awareness training on phishing and malicious attachments