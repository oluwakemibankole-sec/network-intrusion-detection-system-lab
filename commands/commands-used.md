# Commands Used in the NIDS Lab

This file contains important commands used during the implementation of the Network Intrusion Detection System project.

---

# Network Interface Discovery

## Check IP Address and Interfaces

```bash
ip a
```

```bash
ifconfig
```

Purpose:
- Identify active interfaces
- Verify IP addresses
- Determine which interface carries live traffic

---

# Suricata Commands

## Install Suricata

```bash
sudo apt install suricata -y
```

## Verify Installation

```bash
suricata --build-info
```

## Start Suricata

```bash
sudo suricata -c /etc/suricata/suricata.yaml -i <interface>
```

Purpose:
- Launch the intrusion detection engine
- Monitor traffic on the selected interface

---

# View Suricata Logs

```bash
sudo tail -f /var/log/suricata/fast.log
```

Purpose:
- Monitor IDS alerts
- Review suspicious traffic events

---

# Nmap Attack Simulation

## TCP Connect Scan

```bash
nmap -Pn -sT <target-ip>
```

Purpose:
- Simulate reconnaissance activity
- Identify reachable services and open ports

---

## Vulnerability Script Scan

```bash
nmap --script vuln <target-ip>
```

Purpose:
- Simulate vulnerability discovery attempts
- Generate suspicious traffic for analysis

---

# Wireshark Filters Used

## Display TCP Traffic

```bash
tcp
```

## Show SYN Packets

```bash
tcp.flags.syn == 1
```

## Show Reset Packets

```bash
tcp.flags.reset == 1
```

## Combined SYN and Reset Analysis

```bash
tcp.flags.syn == 1 || tcp.flags.reset == 1
```

Purpose:
- Analyze TCP behavior
- Identify reconnaissance traffic patterns
- Detect scanning behavior

---

# Project Workflow Summary

1. Configure virtual machines
2. Identify active interfaces
3. Start Suricata monitoring
4. Launch Wireshark packet capture
5. Simulate attacks using Nmap
6. Capture and analyze suspicious traffic
7. Document findings and screenshots
