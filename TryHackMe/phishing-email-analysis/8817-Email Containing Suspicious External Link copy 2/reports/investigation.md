# Detailed Investigation Report

## Alert Details

| Field | Value |
|---|---|
| Alert ID | 8817 |
| Alert Name | Inbound Email Containing Suspicious External Link |
| Severity | Medium |
| Category | Phishing |
| Timestamp | 05/11/2026 12:18:18.802 |
| Sender | no-reply@m1crosoftsupport.co |
| Recipient | c.allen@thetrydaily.thm |
| Subject | Unusual Sign-In Activity on Your Microsoft Account |
| Attachment | None |
| Direction | Inbound |

---

## Email Content

```html
Hi C.Allen,

We detected an unusual sign-in attempt on your Microsoft account.

Location: Lagos, Nigeria

IP Address: 102.89.222.143

Date: 2025-01-24 06:42

If this was not you, please secure your account immediately to avoid unauthorized access.

<a href="https://m1crosoftsupport.co/login">Review Activity</a>

Thank you,

Microsoft Account Security Team
```

---

# Investigation Steps

## 1. URL Analysis in Splunk

Searched the following URL in Splunk logs:

```text
https://m1crosoftsupport.co/login
```

### Result

- Connection action status: Allowed
- The email was not blocked by security controls.
- Potential risk exists if the user interacted with the link.

---

## 2. URL Reputation Analysis

Analyzed URL:

```text
https://m1crosoftsupport.co/login
```

Using:
- TryDetectThis

### Result

- Reputation status: Malicious
- URL identified as phishing infrastructure.

---

# Analysis

The email impersonates Microsoft account security services and attempts to trick the user into clicking a malicious login page.

## Suspicious Characteristics Observed

- Typosquatted domain `m1crosoftsupport.co` impersonating Microsoft.
- Fear-based social engineering regarding suspicious sign-in activity.
- Fake account compromise notification.
- Malicious phishing URL confirmed by TryDetectThis.
- External IP address included to increase legitimacy.

## Potential Impact

If the user accessed the phishing page and entered credentials, account compromise may occur.

---

# Recommended Actions

- Force password reset / credential rotation for the affected user.
- Block sender domain `m1crosoftsupport.co`.
- Block malicious IP address `102.89.222.143`.
- Review authentication logs for suspicious login activity.
- Monitor for additional phishing attempts targeting users.

---

# Final Verdict

## Classification: True Positive

The email is a confirmed phishing attempt leveraging a malicious typosquatted domain impersonating Microsoft.