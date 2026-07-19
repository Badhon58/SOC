# Phishing

_Objective_ : Phishing is the act of attempting to obtain sensitive information from individuals by using social engineering tactics over various communication platforms such as email, SMS, phone calls, and the internet.

- _Impersonation_
  - Posing as legitimate organizations or individuals
- _Stealing sensitive information_
  - Passwords, credit card numbers, sensitive files
- _Deliver and install Malware_
  - Via attachments, embedded files, or URLs
- _Exploiting humans_
  - Preys on emotions
  - Human psychology

- **How Does Phishing Work?**
  - _Authority_
    - Spoofing executives, managers, IT staff
  - _Trust_
    - Spoofing customers, banks, partners
  - _Intimidation_
    - Instill a sense of fear of consequences
  - _Social Proof_
    - Validate Legitimacy6 through consensus
  - _Urgency_
    - "Act NOW !"
  - _Scarcity_
    - Install a fear of missing out
  - _Familiarity_
    - Establish credibility through recognition

<!-- - ## **Phishing Case Studies** -->

---

## Phishing Attacks Studies

- _Information Gathering_
  - Collecting data through reconnaissance
  - Verify existing accounts, craft credible phished
- _Credential harvesting_
  - Obtain login credentials from victims
  - Fake login pages, deceptive URls
- _Malware Delivery_
  - Malicious attachments or links
  - Drive-by Downloads
- _Spear Phishing_
  - Targeted and customized phishing
  - Research specific individuals or organizations
- _Whaling_
  - Targeting high-profile individuals (CEOs, executives)
- _Vishing, SMiShing and Quishing_
  - Attempts to obtain information over the phone
  - SMS messages containing malicious URLs
  - OR codes leading to malicious URLs
- _Business Email Compromise (BEC)_
  - Compromising legitmate email accounts
  - Unauthorized wire transfers, invoice scams
- _Spam_
  - Unsolicated, irrelevant, and unwanted email
  - Not typically with malicious intent

---

<!-- - **Phishing Attack Techniques** -->

## Phishing Analysis Methodology

- _Initial Triage_
  - Quickly assess and prioritize
- _Header and Sender Examination_
  - Investigate MTAs, addresses, IPs, etc
  - Identify the true origin and check authenticity
- _Content Examination_
  - Analyze email content for language, formatting etc.
  - Look for social engineering red flags
- _Web and URL Examination_
  - Collect web artifacts
  - Utilize tools to inspect URLs and domains
- _Attachment Examination_
  - Security extract and analyze attachments
  - Checking file reputation and sand boxing
- _Contextual Examination_
  - Consider broader context, recent or current incidents
  - Look for patterns and assess scope
- _Defense Measures_
  - Take reactive defense actions
  - take proactive defense actions
  - Communicate with users and stakeholders
- _Documentation and Reporting_
  - Maintain records of findings, verdicts, and actions taken through detailed reports
  - Close out alerts and tickets

---

## Email Header and Sender Analysis

- Download the Email Message
- Install sublime text editor, then open the email with sublime text
- The install a package in sublime text editor
  - tool-> install package control -> ctrl+shift+p -> search "Install package" -> email header
  - After the look at the plan text in bottom -> Click it -> Open Email header
- _iana_ -> Internet Assigned Numbers Authority
- _Email Headers Check_ : https://mha.azurewebsites.net/
- _Email Check_ : https://whois.domaintools.com/

---

## Email Authentications Methods

There are three major email Authentication Technologies out there. We have **SPF, DKIM, and Demar**. And using these protocol, we can check if a domain actually did send and email and essentially identify potential email spoofing. So we have SPF or te sender policy framework .

- **What is SPF?**

- **SPF (Sender Policy Framework)** is an email authentication protocol that helps prevent _email spoofing_ by specifying which mail servers are authorized to send emails on behalf of a domain.

- **How SPF Works**
  - The sender's domain publishes an _SPF record_ as a _DNS TXT record_.
  - When an email is received, the recipient's mail server queries the sender's DNS for the SPF record.
  - The server compares the sender's _IP address_ with the authorized IPs listed in the SPF record.
  - If the IP matches, the email _passes_ the SPF check; otherwise, it _fails_.
    - ✅ _SPF Pass:_ The sender's IP is authorized.
    - ❌ _SPF Fail:_ The sender's IP is unauthorized, so the email may be rejected, quarantined, or marked as spam.

- _DomainKeys Identified Mail (DKIM)_
- _Domain-based Message Authentication, Reporting & Conformance (DMARC)_

---

## Email Content Analysis

- Just review THe context base 64/ html

---

## Anatomy of a URL

The URL => https://academy.tcm-sec.com/cources/example.php?t=129

- _https://_ : Protocol
- _academy.tcm-sec.com_ : Hostname
  - _academy_ : Subdomain
  - _tcm-sec_ : Domain
  - _.com_ : TLD
- _/courses/example.php_ : Path
  - _courses_ : Subdirectory
  - _/example.php_ : File
- _?t=129_ : Parameter

---

## Email URL Analysis

- _quoted-printable_ : THat encode the URL. Split the URL in multiple Line
- https://gchq.github.io/CyberChef/

---

## Email Attachment Analysis

After hash to file we need to check the has is virus or not

- virustotal.com
- sha256sum quotation.iso
- sha1sum quotation.iso
- md5sum quotation.iso
- On windows its

```bash
$ get-filehash .\quotation.ios
$ get-filehash .\quotation.ios -algorithm md5
$ get-filehash .\quotation.ios -algorithm sha1

# Get all file hashes
$ get-filehash .\quotation.ios; get-filehash .\quotation.ios -algorithm sha1; get-filehash .\quotation.ios -algorithm md5;

# Check all the hash in the virustotal.com website
# And https://www.talosintelligence.com/
```

---

## Dynamic Attachment Analysis and Sand boxing

- When performing the dynamic analysis we are looking for 4 common things. So the first is the process activity.

1. **Process Activity**
2. **Registry Activity**
3. **Network Connection**
4. **File Activity**

- Tools for analysis for Malware
  - _hybrid-analysis.com_
  - _joesandbox.com_
  - _anyrun.com_
