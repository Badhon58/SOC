## Intrusion Detection with Suricata

Network Intrusion Detection with Suricata

install suricata

Config the file

```bash

# Check Suricata
$ sudo systemctl stop/start/status suricata.service

# Suricata File
$ sudo vim /etc/suricata/suricata.yaml

# Changed on line 12 var ad home subnet address
$ ipconfig
$ ip a s

# Changed the interface at line 580
af-packet:
    - interface: enp0s3

# Changed also libpcap
pcap:
    - interface : enp0s3

# Changed the rule Path line 1872
default-rule-path : /var/lib/suricata/rules
rule-files:
    - suricata.rules
    - /path/local.rule

# Apply the Changed
$ sudo suricata-update

# List directory of suricata file
$ sudo ls -al /var/lib/suricata/rules

#  Custom Rules
$ sudo vim /etc/suricata/rules/local.rule
    alert icmp any any -> $HOME_NET (msg: "ICMP Ping"; sid:1; rev:1;)

# Check Any problem are there
$ sudo suricata -T -c /etc/suricata/suricata.yaml -v
$ sudo cat /var/log/suricata/fast.log
$ sudo cat /var/log/suricata/eve.log

```

## Integration Suricata with wazuh
