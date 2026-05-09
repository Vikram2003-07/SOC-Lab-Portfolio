# SOC-Lab-Portfolio

A comprehensive repository documenting my technical proficiency in Security Operations Center (SOC) workflows, incident response, and threat analysis. This portfolio serves as a centralized knowledge base for my investigative methodologies and findings derived from hands-on labs in environments like TryHackMe and LetsDefend.

## 🛡️ Core Competencies & Analysis Types

This repository is organized by analytical domains to demonstrate a structured approach to threat hunting and incident investigation:

### 🔍 Malware Analysis
Detailed breakdowns of malicious software behavior, including:
* **Static Analysis:** File fingerprinting (hashes), string analysis, and header inspection.
* **Dynamic Analysis:** Behavioral monitoring in sandboxed environments, API call tracking, and network communication patterns.
* **Persistence Mechanisms:** Identifying how malware maintains presence within a system.

### 📧 Phishing Analysis
End-to-end investigation of email-based attacks, covering:
* **Header Analysis:** Investigating SPF, DKIM, and DMARC records to identify spoofing.
* **URL/Link Investigation:** Analyzing obfuscated URLs and redirection chains.
* **Attachment Scrutiny:** Examining malicious payloads and macro-enabled documents.

### 📁 Malicious File Analysis
Deep dives into suspicious artifacts, including:
* **File Integrity:** Analyzing file types, magic bytes, and entropy.
* **Execution Flow:** Tracing how malicious files interact with the OS and registry.
* **IOC Extraction:** Documenting Indicators of Compromise (IPs, Domains, Hashes) for defensive implementation.

---

## 📂 Repository Structure

The documentation is categorized by platform and investigation type for easy navigation:

```bash
├── TryHackMe/
│   ├── Malware-Analysis/
│   ├── Phishing-Investigations/
│   └── [Other-Topics]/
├── LetsDefend/
│   ├── Incident-Response-Reports/
│   ├── Endpoint-Analysis/
│   └── [Other-Topics]/
```

## 🛠️ Tools & Technologies

Throughout these reports, I utilize a professional security stack, including but not limited to:
* **Analysis Tools:** Wireshark, Any.Run, VirusTotal, Procmon, PEStudio.
* **SIEM/EDR Concepts:** Log analysis, alert triage, and endpoint telemetry.
* **Operating Systems:** Windows (Forensics/Registry), Linux (Command Line/Log analysis).

## 🚀 Objective
My goal is to demonstrate a disciplined, evidence-based approach to cybersecurity investigations, transforming raw telemetry into actionable intelligence and clear, professional reporting.