# Class 4 | Alert Triage, TTPs & Threat IOCs

## TTPs (Tactics, Techniques, and Procedures) in SOC

They describe how attackers think, act, and operate during a cyber attack. _If an IOC Tells you what happened TTPs tell you how and why it happened_.

- _SOC analysts use TTPs to_
  - Detect attacks even when IOCs change.
  - Understand attacker intent
  - Build better detections, alerts and response playbooks

---

## TACTICS - The Goal / The Target

Tactics describe WHY the attacker is doing something.Each tactic represent a phase of the attack lifecycle.

- _Common attacker goals_
  - Gain initial access
  - Steal credentials
  - Move laterally
  - Exfiltrate data
  - Maintain persistence

- _Tactics - Example_

| _Tactic_             | _Meaning_                  |
| -------------------- | -------------------------- |
| Initial Access       | How attacker first gets in |
| Execution            | Running malicious code     |
| Persistence          | Staying in the system      |
| Privilege Escalation | Becoming admin             |
| Defense Evasion      | Avoiding Antivirus/EDR     |
| Lateral Movement     | Moving to other systems    |
| Ex filtration        | Stealing data              |

---

## Techniques - The Method / The Planing

Techniques describe HOW the attacker achieves a tactic. Think of techniques as specific attack methods. For Example

- _Tactic_ : Credential Access
- _Techniques_ :
  - key logging
  - Credential dumping (LSASS)
  - Browser password theft
  - Phishing for credentials

---

## Procedures - The Exact Steps

Procedures are the attacker's exact implementation in the real world.

- _The is where_
  - Tools
  - Commands
  - Scripts
  - Timing etc come into play
- Example : **Technique** Credential Dumping.

---

## IOCs = Indicators of Compromise

They are observable evidence that suggests a system may be compromised or under attack. If TTPs describe attacker behavior. IOCs are the footprints attackers leave behind.

SOC analysts hunt detect, correlate, and respond using IOCs every single day.
IOC = _Something bad happened here, and we can prove it with data_.

- _That "data" comes from_
  - Logs
  - Network traffic
  - Endpoint activity
  - Email headers
  - File systems

- _In a real SOC environment, IOCs help you_
  - Trigger alerts in SIEM
  - Confirm malicious activity
  - Correlate attacks across systems
  - Respond quickly (block)
  - Write incident reports.

### Types of IOCs

1. **_Network Based IOCs_**
   This show what happened inside the network.

- _Example_
  - Malicious IP address
  - Suspicious domain
  - C2 server communication
  - Unusual ports or protocols
- _Where SOC Sees Them_
  - Firewall Logs
  - proxy logs
  - DNS logs
  - IDS/IPS alerts

2. **_Host/Endpoint-based IOCs_**
   These show what happened inside the system

- _Example_
  - Suspicious processes
  - Unexpected services
  - Registry changes
  - New scheduled tasks
- _Where SOC Sees Them_
  - EDR/XDR
  - Windows Event logs
  - Sysmon
  - Linux audit logs

3. **_File-based IOCs_**
   These relate to malicious files

- _Example_
  - File hash (MD5, SHA256)
  - File name patterns
  - File size anomalies
- _Where SOC Sees Them_
  - Antivirus
  - EDR
  - Email security gateways
  - Sandboxes

4. _Email-based IOCs_
   THese relate to malicious emails
