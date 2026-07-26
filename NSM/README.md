# Network Security Monitoring (NSM)

=> Need to Learn ZEEK, Snort, Suricata

- _Some rule in NSM_
  - IDS = Instruction Detection Systems - Alert, Log
  - IPS = Instruction Preventions System - Drop, Reject
  - NIDS = Network Instruction Detection Systems - Scope Of Network
    NIPS = Network Instruction Preventions System - Scope Of Network
    HIDS
    HIPS

- _Rules_
  1. Signatures Based
  2. Behaver Based
  3. Policy Based
- Normal - TCP and UDP
- Abnormal - FTP

## Snort

- Snots Need Rules
- It is an IDS/IPS Alone
- Snort Can Analysis Live Traffic
  - Alerts, Logs, Drops, Rejects
- Log Packets
- Prevent Threats
  - Alerts, Logs, Drops, Rejects

- **Configuration**
  1. Configuration Files : It contain path to rules. Location /etc/snort/snort.conf
  2. Plugins
  3. Sources Network : Home
  4. External Network : Any

- **Rules**
  1. /etc/snort/local.rules

- **Snort Modes**
  - Sniffer Mode
  - Packet Logger
  - NIDS/NIPS

- _Start the Snort to the Sniffer Mode_
  - 

---

## ZEEK

- Open Sources - Networking Monitoring
  - UpTime
  - Devices Health
  - Connection Quality
  - Performances
