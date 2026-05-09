# 🔍 Detailed Analysis – AsyncRAT Phishing Incident

## 📧 Email Analysis

The email originated from **[free@coffeeshooop.com](mailto:free@coffeeshooop.com)**, a suspicious domain exhibiting typosquatting behavior. The subject “Free Coffee Voucher” was used as a lure to trick the recipient into opening the attachment.

### Red Flags:

* Misspelled domain (**coffeeshooop**)
* Suspicious attachment (`free-coffie.zip`)
* Unsolicited reward-based email

---

## 📦 Attachment Analysis

The ZIP file contained an executable named **coffee.exe**.

Upon execution:

* The file deployed **AsyncRAT malware**
* Established persistence mechanisms
* Attempted outbound communication

---

## 🧪 Malware Behavior

Analysis via sandbox environment revealed:

* Execution of malicious process (`coffee.exe`)
* Network beaconing to external IP
* Indicators consistent with **Remote Access Trojan (RAT)** activity

---

## 🌐 Network Analysis

* **C2 IP:** 37.120.233.226
* Malware attempted communication with command-and-control server
* Indicates active attacker control capability

---

## 🔑 Indicators of Compromise (IOCs)

| Indicator Type | Value                                                 |
| -------------- | ----------------------------------------------------- |
| IP Address     | 37.120.233.226                                        |
| Domain         | coffeeshooop.com                                      |
| Email          | [free@coffeeshooop.com](mailto:free@coffeeshooop.com) |
| MD5 Hash       | 73F0F77181E1F06A9DBC41EA9E7A03FE                      |

---

## ⚠️ Impact Analysis

If left undetected, AsyncRAT could:

* Allow remote control of infected system
* Capture keystrokes and credentials
* Exfiltrate sensitive data
* Spread laterally within the network

---

## 🛡️ Incident Response

The following actions were taken:

* Infected host was **isolated (contained)**
* Phishing email was **removed from mailbox**
* Malicious IP/domain were **blocked**
* System marked for **rebuild (nuke and pave)**
* All active sessions were **terminated**
* User credentials were **reset**

---

## 🧠 Analyst Conclusion

This incident was a successful phishing attempt leading to execution of AsyncRAT malware. Quick detection and containment prevented further damage.

The attack highlights the importance of:

* User awareness against phishing
* Email filtering mechanisms
* Rapid SOC response procedures

---