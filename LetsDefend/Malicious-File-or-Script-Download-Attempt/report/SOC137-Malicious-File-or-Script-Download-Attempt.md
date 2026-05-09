# Investigation Report - SOC137 Alert

## 🧠 Alert Description
The SOC137 alert indicates an attempt to download a malicious file or script. The file involved is a macro-enabled Word document, often used in phishing attacks to execute malicious code.

---

## 📂 File Analysis

- **File Name:** INVOICE PACKAGE LINK TO DOWNLOAD.docm  
- **Hash (MD5):** f2d0c66b801244c059f636d08a474079  

### 🔎 VirusTotal Results
- **Detection Ratio:** 37 / 64 vendors flagged as malicious  
- **Threat Label:** trojan.sagent / vpnz  

### 📌 Observations
- The file is a **.docm (macro-enabled document)**, indicating potential macro execution.
- Common tactic: trick user into enabling macros → execute payload.
- Likely delivered via phishing email disguised as invoice-related content.

---

## 💻 Endpoint Analysis

- No communication with Command & Control (C2) servers detected.
- Indicates:
  - File execution likely prevented, OR
  - Infection stopped at early stage.

---

## 🚫 Security Control Actions

- **File download was blocked** by security controls.
- No further spread or lateral movement observed.

---

## ⚠️ Threat Assessment

| Indicator              | Status         |
|----------------------|---------------|
| Malicious File       | ✅ Confirmed   |
| Execution            | ❌ Prevented   |
| C2 Communication     | ❌ Not observed|
| Lateral Movement     | ❌ Not observed|

---

## 🧾 Conclusion

This alert is a **True Positive**.  
The file is confirmed malicious and matches known trojan signatures. Security controls effectively prevented execution and potential compromise.

---

## 🔐 Recommendations

1. Disable macros in Microsoft Office by default.
2. Implement email filtering for suspicious attachments.
3. Conduct user awareness training on phishing attacks.
4. Monitor endpoints for similar indicators (hash, filename).
5. Use sandboxing for suspicious file analysis.

---

## 📌 MITRE ATT&CK Mapping

- **T1566.001** – Phishing: Spearphishing Attachment  
- **T1204.002** – User Execution: Malicious File  
- **T1059.005** – Command Execution via Macros  

---