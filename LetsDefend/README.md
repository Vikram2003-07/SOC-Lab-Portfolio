# SOC Reports - LetsDefend

Central collection of SOC investigation writeups and lab exercises from LetsDefend scenarios. Reports are grouped by analysis category and case folder.

## Quick Overview

- **Purpose:** Learning and documenting SOC triage, analysis, and reporting workflows.
- **Content:** Case notes, screenshots, investigation steps, and final incident reports.

## Top-level Folders

- `Malware-analysis/` — Malware-focused investigations (detection, sandboxing, IOC extraction, remediation notes).
- `phishing-email-analysis/` — Phishing email investigations (headers, attachments, URLs, user impact, remediation).

## Table of contents (by case)

Malware-analysis:

- `SOC104 - Malware Detected` — analyst note and final report (see Malware-analysis/SOC104 - Malware Detected/report/soc104-Malware-Detected.md)
- `SOC109 - Emotet Malware Detected` — analyst note and final report (see Malware-analysis/SOC109 - Emotet Malware Detected/report/soc109-Emotet-Malware-Detected.md)
- `SOC119 - Proxy - Malicious Executable File Detected` — analyst note and final report (see Malware-analysis/SOC119 - Proxy - Malicious-Executable-File-Detected/report/soc119-Proxy-Malicious-Executable-File-Detected.md)

Phishing-email-analysis:

- `SOC114 - Malicious Attachment Detected - Phishing Alert` — analyst notes and report (phishing-email-analysis/SOC114 - Malicious Attachment Detected - Phishing Alert/reports/soc114-malicious-attachment.md)
- `SOC120 - Phishing Mail Detected Internal to Internal` — analyst note and report (phishing-email-analysis/SOC120 - Phishing Mail Detected Internal to Internal/reports/soc120-Phishing-Mail-Analysis.md)
- `SOC140 - Phishing Mail Detected - Suspicious Task Scheduler` — analyst note and report (phishing-email-analysis/SOC140 - Phishing Mail Detected - Suspicious Task Scheduler/reports/soc140-Phishing-Mail-Analysis.md)
- `SOC141 - Phishing URL Detected` — analyst notes and report (phishing-email-analysis/SOC141 - Phishing URL Detected/reports/soc141-phishing-url-analysis.md)
- `SOC282 - Phishing Alert Deseptive Mail Detected` — analyst notes and report (phishing-email-analysis/SOC282 - Phishing Alert Deseptive Mail Detected/reports/soc282-phishing-mail-analysis.md)

## How to use this workspace

1. Open a case folder (for example, `phishing-email-analysis/SOC114 - Malicious Attachment Detected - Phishing Alert`).
2. Review `analyst-note.md` / `analyst-notes.md` for investigation steps and evidence.
3. See the final incident report in each case's `report/` or `reports/` subfolder for a concise summary.

## Suggested next steps

- Review and standardize individual case `README.md` files to include TL;DR, timeline, and key IOCs.
- Add a small index file linking directly to each final report for quicker navigation.
