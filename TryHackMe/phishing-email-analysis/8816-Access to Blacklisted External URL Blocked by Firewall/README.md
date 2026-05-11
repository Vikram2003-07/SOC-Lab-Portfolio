# Access to Blacklisted External URL Blocked by Firewall - Investigation

## Alert Information

- **Alert ID:** 8816
- **Alert Name:** Access to Blacklisted External URL Blocked by Firewall
- **Severity:** Medium
- **Category:** Malicious URL Access
- **Date:** May 11, 2026

## Objective

Investigate the firewall alert related to an attempt to access a blacklisted external URL and determine whether further action is required.

## Investigation Summary

The investigation included:
- Reviewing firewall logs
- Verifying whether the connection attempt was blocked
- Analyzing the URL reputation using TryDetectThis
- Assessing the impact of the attempted connection

## Key Findings

- The connection attempt to the URL was successfully blocked by the firewall.
- The URL `http://bit.ly/3sHkX3da12340` was identified as malicious in TryDetectThis.
- No successful outbound communication was established.
- Existing security controls functioned as intended.

## Final Verdict

**True Positive**

The URL is confirmed malicious; however, the firewall successfully blocked the connection attempt. No further escalation is required at this time.

## Files Included

- `investigation.md` → Detailed investigation process and findings
- `analyst-note.md` → Short SOC analyst case summary