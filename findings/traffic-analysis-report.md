# Traffic Analysis Report

## Project Summary

This report documents the analysis of suspicious network traffic captured during the implementation of a Network Intrusion Detection System (NIDS) lab.

The environment consisted of:
- Kali Linux (attacker machine)
- Metasploitable (target system)
- Ubuntu (monitoring workstation)

Wireshark and Suricata were used to monitor and analyze traffic generated during simulated reconnaissance activity.

---

# Objective

The objective of the analysis was to:
- capture live network traffic,
- identify suspicious packet behavior,
- analyze TCP communication patterns,
- and determine whether reconnaissance activity occurred.

---

# Attack Simulation

Reconnaissance traffic was generated using Nmap from the Kali Linux system.

Commands used:

```bash
nmap -Pn -sT <target-ip>
nmap --script vuln <target-ip>
```

These scans were directed toward the Metasploitable target machine.

---

# Packet Capture and Analysis

Traffic was captured using Wireshark on the active monitoring interface.

The following protocols were observed:
- TCP
- ARP
- DNS
- ICMPv6

The most significant finding was the presence of repeated TCP SYN packets followed by RST/ACK responses.

---

# Detection Evidence

## TCP SYN and RST/ACK Analysis

The packet capture showed:
- repeated SYN packets,
- connection attempts across multiple ports,
- and RST/ACK responses from the target system.

This behavior is commonly associated with:
- reconnaissance activity,
- port scanning,
- and unauthorized service discovery attempts.

---

# Key Findings

- Live traffic was successfully captured in the lab environment.
- TCP packet behavior consistent with scanning activity was identified.
- Interface troubleshooting was required to identify the active monitoring interface.
- Wireshark filtering improved visibility into suspicious traffic patterns.

---

# Challenges Encountered

Several challenges occurred during implementation:
- incorrect interface selection,
- inconsistent traffic visibility,
- and Suricata alert inconsistency in the virtual environment.

These issues were resolved through:
- interface comparison,
- packet-level analysis,
- and monitoring adjustments.

---

# SOC Analyst Interpretation

From a SOC analyst perspective, the observed traffic pattern indicates suspicious reconnaissance activity.

Repeated SYN packets and reset responses suggest that the scanning system was attempting to identify open services on the target machine.

In a production environment, this activity would require:
- investigation,
- source IP verification,
- alert correlation,
- and potential containment actions.

---

# Recommendations

Recommended improvements include:
- integrating Suricata with Splunk or ELK,
- implementing IPS functionality,
- creating custom Suricata rules,
- and expanding the lab to include brute-force attack simulations.

---

# Conclusion

The project successfully demonstrated how suspicious network traffic can be captured, analyzed, and interpreted using a Network Intrusion Detection System lab.

The findings support the conclusion that reconnaissance-style scanning behavior was successfully simulated and identified through packet analysis.

This project demonstrates foundational SOC analyst skills including:
- packet analysis,
- network monitoring,
- traffic investigation,
- and technical reporting.
