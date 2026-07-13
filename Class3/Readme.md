# System Attack Vectors & Vulnerabilities

## Core Concept

### The 3 SOC Operating Models

1. **In House (Internal) SOC**
   A company builds and runs its own soc internally using its own people, tools, and process.

![The 3 SOC Operating Models](./Image/SOC%20TS.png)

2. **Outsourced / Managed SOC (MSP/MSSP SOC)**
3. **Hybrid SOC (Co - Managed SOC)**

---

# System As Attack Vectors

If you understand systems as attack vectors, you stop being a beginner and start thinking like an analyst. In SOC, we don't just protect users or data, we protect systems, because every system can be abused as an attack vector

- _A System becomes as attack vector when an attacker uses it to_
  - Gain initial access
  - Move laterally
  - Maintain Persistence
  - Exfiltrate data
  - Launch further attacks

---

## Human Oriented Attacks

Users are those who start the attack mostly : (Before external factors, Users are responsible at first)

By inserting a malicious USB found ona street, downloading malware from pirated resources, or simply reusing a weak password everywhere, 81% of breaches involve stolen or breached passwords.

- _Example_:
  - Rubber Ducky
  - Key loggers binded with legitimate softwares.
  - Clicking on suspicious links.
  - Opening any email or sent attachments.
  - Storing passwords at unsecure portals
  - Trusting soon
  - Using outdated/pirated softwares etc.

---

## Supply Chain Attacks

Your PC is home to hundreds of apps, including web browsers, messengers, development, and entertainment software. Every app downloads on thousands of libraries

If threat actors manage to breach one of the apps or libraries and push an update to all its users. all of them will be compromised. This technique is called a supply chain attack. The most famous examples are the solarwinds and 3CX breaches which affected thousands of companies.

It is hard to protect from supply chain attacks since you can't always control all the software present on your laptops, servers, and web apps.

---

## Vulnerabilities

A vulnerability is a weakness in a system, software, hardware, or process that can be exploited by an attacker to gain access, Escalate code. Steal data, Disrupt services & more...

_A vulnerability is a flow or weakness in a system that can be exploited to compromise confidentiality, integrity, or availability_

Vulnerabilities can exist in Software, OS, Applications, Network Devices, Firmware's, Cloud Services or even Security Software Solutions.

---

## Software Vulnerabilities

Once a vulnerability is made public, It is assigned a Common Vulnerabilities and Exposures (CVE) number.

- _Example of Software Vulnerabilities_:
  - SQL Injection
  - Command Injection
  - Buffer Overflow
  - Cross-Site Scripting (XSS)
  - Remote Code Executions (RCE)

- _SOC detection_
  - WAF alerts
  - Web server logs
  - Unusual POST requests
  - EDR alerts on servers

---

## OS Vulnerabilities

- _Example of OS Vulnerabilities_
  - Windows Vulnerabilities
  - Linux Vulnerabilities
  - mac OS Kernels or services Vulnerabilities

For Example: Privilege escalation bugs, SMB Vulnerabilities(Eternal-Blue), Kernel exploits etc

- _SOC Detection_
  - Sudden privilege changes
  - Exploit behavior in EDR
  - Kernel driver loading alerts etc...

---

## Network Vulnerabilities

- _Example of Network Vulnerabilities_
  - Open ports
  - Weak protocols(Telnet, FTP)
  - Unpatched routers/firewalls
  - Exposed admin interfaces

- _SOC Detection_
  - IDS/IPS alerts
  - Firewall logs
  - Excessive authentication failures

---

## Authentication & Authorization Vulnerabilities

- _Example of Authentication & Authorization Vulnerabilities_
  - Weak passwords
  - No MFA
  - Broken access control
  - Privilege escalation paths

- _SOC Detection_
  - IAM alerts
  - Access logs
  - Role change events

---

## Configuration-Dependent Vulnerabilities

- _Example of Configuration-Dependent Vulnerabilities_
  - Debug mode enabled
  - Default credentials
  - Excessive Permissions

- _SOC Detection_
  - Admin panel exposed
  - Default credentials unchanged
  - System takeover

---

## Zero Day Vulnerabilities

A vulnerability which patch does not exist yet as it unknown to the vendor yet and are used by malicious actors like hackers

- _SOC Detection_
  - Abnormal processes
  - Suspicious network traffic
  - Lateral movement

---

## Zero-Day Vulnerabilities

- _Life cycle of a zero day_
  - A new Vulnerability is discovered
  - A method to exploit the vulnerability discovered.
  - Cyber criminals leverage the vulnerability to cause damage
  - Vulnerability discovered by the software vendors
  - Patch release by the software vendors

---

## Endpoints

-> Major System categories Used as attack Vectors

- _What is Endpoint Security?_
  - The policies, processes and technology control used to protect the confidentiality, integrity and availability of an endpoint system.
    - Anti malware
    - Endpoint Security control
    - Application Security
    - IAM
    - Acceptable use Policies
    - Configuration Management
    - System Monitoring
    - Anti Malware
