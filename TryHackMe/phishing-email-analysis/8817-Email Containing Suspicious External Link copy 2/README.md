# Inbound Email Containing Suspicious External Link - Investigation

## Alert Information

- **Alert ID:** 8817
- **Alert Name:** Inbound Email Containing Suspicious External Link
- **Severity:** Medium
- **Category:** Phishing
- **Date:** May 11, 2026

## Objective

Investigate the inbound email containing a suspicious Microsoft account security notification and determine whether the email is malicious.

## Investigation Summary

The investigation included:
- Reviewing the embedded URL activity in Splunk
- Verifying URL reputation using TryDetectThis
- Identifying phishing indicators within the email
- Assessing potential impact to the user account

## Key Findings

- The embedded URL was allowed through security controls.
- The URL `https://m1crosoftsupport.co/login` was identified as malicious in TryDetectThis.
- The sender domain `m1crosoftsupport.co` impersonates Microsoft using typosquatting.
- The email used fear-based social engineering tactics related to account compromise.
- User credential exposure risk exists if the link was accessed.

## Recommended Actions

- Force password reset / credential rotation for the affected user.
- Block the malicious sender domain.
- Block the associated malicious IP address.
- Monitor for suspicious login attempts related to the user account.

## Final Verdict

**True Positive**

The email is a confirmed phishing attempt impersonating Microsoft account security notifications.

## Files Included

- `investigation.md` → Detailed investigation process and findings
- `analyst-note.md` → Short SOC analyst case summary