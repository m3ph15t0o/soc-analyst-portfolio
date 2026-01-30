# 🚨 Case Study #1: Suspicious SSH Data Transfer (PCAP Investigation) – BTLO (Simulated)

## 📌 Summary
This case study is based on a **Blue Team Labs Online (BTLO)** simulated PCAP investigation.
The goal was to identify suspicious SSH traffic, estimate transferred data volume, and attribute infrastructure using OSINT.

---

## 🎯 Objectives
- Identify remote IP used for SSH transfer
- Estimate total data transferred
- Attribute infrastructure (ASN + hosting provider)
- Map to MITRE ATT&CK
- Provide SOC response recommendations

---

## 🧰 Tools Used
- Wireshark
- OSINT (ASN lookup, provider checks)
- Threat Intel (optional)

---

## 🧾 Key Findings
| Indicator | Value |
|----------|-------|
| Remote IP (SSH) | 35.211.33.16 |
| Data transferred | 1131 MB (~1.13 GB) |
| Malware family | TrickBot |
| Suspicious ASN(s) | AS14061, AS63949 |
| Category | Crypto Miner-related |

---

## 🧠 MITRE ATT&CK Mapping
- T1496 – Resource Hijacking  
- T1071.004 – DNS  
- T1021.004 – SSH  

---

## ✅ Conclusion
True Positive *(Simulated)*

---

## 🛡️ Recommendations
- Block IP/ASN
- Alert on outbound SSH to unknown external IPs
- Detect transfer spikes
- Isolate host and run EDR scan
