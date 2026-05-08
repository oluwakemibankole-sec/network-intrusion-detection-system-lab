# network-intrusion-detection-system-lab
A SOC-style NIDS lab using Suricata, Wireshark, Kali Linux, Ubuntu, Metasploitable, and Nmap to detect reconnaissance and suspicious TCP traffic.
# Network Intrusion Detection System Lab

## Project Overview
This project demonstrates the design and implementation of a Network Intrusion Detection System lab for monitoring and detecting suspicious network activity.

The lab simulates reconnaissance activity using Kali Linux and Nmap, captures traffic using Wireshark, and analyzes detection evidence using Suricata concepts.

## Objective
- Build a controlled cybersecurity lab environment
- Simulate suspicious network traffic
- Capture and analyze packets
- Identify reconnaissance-style TCP behavior
- Present findings using SOC-style documentation

## Lab Architecture
| Machine | Role | Tools |
|---|---|---|
| Kali Linux | Attacker | Nmap |
| Metasploitable | Target | Vulnerable services |
| Ubuntu | NIDS Sensor | Wireshark, Suricata |

## Tools Used
- VirtualBox
- Kali Linux
- Ubuntu
- Metasploitable
- Nmap
- Wireshark
- Suricata

## Attack Simulation
Nmap was used to simulate reconnaissance against the target machine.

```bash
nmap -Pn -sT <target-ip>
nmap --script vuln <target-ip>

## Project Documents

- [NIDS Defence Slides (PPTX)](docs/nids-project-defence-slides.pptx)
- [NIDS Defence Slides (PDF)](docs/nids-project-defence-slides.pdf)
- [NIDS Project Report](docs/nids-project-report.pdf)
