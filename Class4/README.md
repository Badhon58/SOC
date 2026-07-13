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
