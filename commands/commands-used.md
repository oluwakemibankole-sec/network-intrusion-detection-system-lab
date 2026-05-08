# Commands Used in the NIDS Lab

## Check IP Address and Interfaces

```bash
ip a
ifconfig

nmap -Pn -sT <target-ip>
nmap --script vuln <target-ip>

sudo suricata -c /etc/suricata/suricata.yaml -i <interface>

sudo tail -f /var/log/suricata/fast.log

tcp
tcp.flags.syn == 1
tcp.flags.reset == 1
