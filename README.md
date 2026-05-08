# Network Intrusion Detection System (NIDS) Lab

## Overview

This project demonstrates the design and implementation of a Network Intrusion Detection System (NIDS) lab for monitoring and detecting suspicious network activity.

The lab simulates reconnaissance traffic using Kali Linux and Nmap against a Metasploitable target while Ubuntu monitors traffic using Wireshark and Suricata.

---

# Lab Architecture

| Machine | Role | Tools |
|---|---|---|
| Kali Linux | Attacker | Nmap |
| Metasploitable | Victim/Target | Vulnerable Services |
| Ubuntu | Monitoring Sensor | Wireshark, Suricata |

---

# Tools Used

- VirtualBox
- Kali Linux
- Ubuntu
- Metasploitable
- Wireshark
- Nmap
- Suricata

---

# Attack Simulation

Reconnaissance activity was simulated using Nmap:

```bash
nmap -Pn -sT <target-ip>
nmap --script vuln <target-ip>
```

---

# Detection Evidence

## Wireshark TCP SYN Analysis

Wireshark analysis showing repeated TCP SYN packets followed by RST/ACK responses during simulated reconnaissance activity.

This pattern is consistent with scanning behavior and unauthorized service discovery attempts.

![TCP Analysis](screenshots/08-tcp-syn-rst-analysis.png)

---

# Final Detection Evidence

The final analysis identified repeated TCP SYN packets and reset responses captured on the active monitoring interface.

![Final Evidence](screenshots/09-final-detection-evidence.png)

---

# Live Traffic Capture

Wireshark successfully captured live network traffic including TCP, DNS, ARP and ICMPv6 protocols.

![Live Traffic](screenshots/07-live-traffic-capture.png)

---

# SOC Analyst Skills Demonstrated

- Packet Analysis
- Network Monitoring
- Wireshark Traffic Analysis
- TCP Flag Interpretation
- Reconnaissance Detection
- Linux Administration
- IDS Monitoring
- Troubleshooting
- Technical Reporting

---

# Challenges Encountered

- Incorrect interface selection initially showed limited traffic
- Suricata alert inconsistency in virtualized environments
- Network routing visibility issues in VirtualBox

These issues were resolved through interface analysis and packet-level investigation.

---

# Future Improvements

- Integrate Suricata logs with Splunk or ELK
- Implement IPS functionality
- Add brute-force attack simulations
- Create custom Suricata detection rules

---

# Project Documents

- [NIDS Defence Slides (PPTX)](docs/nids-project-defence-slides.pptx)
- [NIDS Defence Slides (PDF)](docs/nids-project-defence-slides.pdf)
- [NIDS Project Report (PDF)](docs/nids-project-report.pdf)
- [NIDS Project Report (DOCX)](docs/nids-project-report.docx)
- [Traffic Analysis Report](findings/traffic-analysis-report.md)
# Screenshots

## Lab Setup

![Lab Setup](screenshots/01-lab-setup.png)

---

## Suricata Fast Log

![Suricata](screenshots/04-suricata-fastlog.png)

---

## Wireshark Interface Selection

![Wireshark Interface](screenshots/05-wireshark-interface-selection.png)

---

## Live Traffic Capture

![Live Traffic](screenshots/07-live-traffic-capture.png)

---

## TCP SYN and RST Analysis

![TCP Analysis](screenshots/08-tcp-syn-rst-analysis.png)

---

## Final Detection Evidence

![Final Evidence](screenshots/09-final-detection-evidence.png)

---

# Author

**Oluwakemi Bankole**  
Cybersecurity Analyst | SOC Analyst | Penetration Testing Enthusiast
