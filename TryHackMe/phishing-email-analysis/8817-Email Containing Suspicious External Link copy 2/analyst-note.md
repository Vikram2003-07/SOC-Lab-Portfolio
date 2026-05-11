Investigated alert ID 8817 related to a suspicious Microsoft account security email.

Reviewed the URL `https://m1crosoftsupport.co/login` in Splunk and observed the connection action was allowed. Further analysis in TryDetectThis confirmed the URL as malicious.

The email used a typosquatted Microsoft domain and social engineering tactics to lure the user into credential theft.

Recommended actions:
- Rotate affected user credentials
- Block malicious sender domain
- Block associated malicious IP address

Verdict: True Positive.