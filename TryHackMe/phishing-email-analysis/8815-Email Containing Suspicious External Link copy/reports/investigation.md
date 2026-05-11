# Detailed Investigation Report

## Alert Details

| Field | Value |
|---|---|
| Alert ID | 8815 |
| Alert Name | Inbound Email Containing Suspicious External Link |
| Severity | Medium |
| Category | Phishing |
| Timestamp | 05/11/2026 12:16:00.802 |
| Sender | urgents@amazon.biz |
| Recipient | h.harris@thetrydaily.thm |
| Subject | Your Amazon Package Couldn’t Be Delivered – Action Required |
| Attachment | None |
| Direction | Inbound |

---

## Email Content

```html
Dear Customer,

We were unable to deliver your package due to an incomplete address.

Please confirm your shipping information by clicking the link below:

http://bit.ly/3sHkX3da12340

If we don’t hear from you within 48 hours, your package will be returned to sender.

Thank you,

Amazon Delivery
```

---

# Investigation Steps

## 1. URL Analysis in Splunk

Searched the following URL in Splunk logs:

```text
http://bit.ly/3sHkX3da12340
```

### Result

- Security controls blocked the message.
- The URL was identified as suspicious/malicious.
- No successful access to the malicious destination was observed.

---

## 2. URL Reputation Analysis

Analyzed URL:

```text
http://bit.ly/3sHkX3da12340
```

Using:
- TryDetectThis (AnalystVM)

### Result

- Reputation status: Malicious
- URL flagged as phishing/malicious activity.

---

# Analysis

The email impersonates Amazon delivery services and attempts to create urgency by claiming package delivery failure.

## Suspicious Characteristics Observed

- Sender domain `amazon.biz` is not an official Amazon domain.
- Use of URL shortening service (`bit.ly`) to obscure the final destination.
- Urgent social engineering language designed to pressure the recipient.
- Malicious URL confirmed by TryDetectThis analysis.
- Email was blocked by security controls.

These indicators strongly suggest a phishing attempt intended to harvest user information or redirect users to a malicious website.

---

# Final Verdict

## Classification: True Positive

The email contains a confirmed malicious URL and exhibits multiple phishing indicators. The message was appropriately blocked by security controls.