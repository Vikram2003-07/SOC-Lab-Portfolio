# Inbound Email Containing Suspicious External Link - Investigation

## Alert Information

- **Alert ID:** 8815
- **Alert Name:** Inbound Email Containing Suspicious External Link
- **Severity:** Medium
- **Category:** Phishing
- **Date:** May 11, 2026

## Objective

Investigate the inbound email containing a suspicious external link and determine whether the email is malicious or benign.

## Investigation Summary

The investigation included:
- Reviewing the suspicious URL in Splunk
- Verifying whether the message was blocked
- Analyzing the embedded link using TryDetectThis in AnalystVM
- Identifying phishing indicators within the email

## Key Findings

- The embedded URL used a shortened `bit.ly` link.
- Splunk logs confirmed the message was blocked by security controls.
- TryDetectThis classified the URL as malicious.
- The sender domain `amazon.biz` is suspicious and not associated with the legitimate Amazon domain.
- The email used urgency and delivery failure themes commonly associated with phishing attacks.

## Final Verdict

**True Positive**

The email was confirmed to contain a malicious phishing URL and was successfully blocked by security controls.

## Files Included

- `investigation.md` → Detailed investigation process and findings
- `analyst-note.md` → Short SOC analyst summary note