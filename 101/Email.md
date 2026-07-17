## Email

1. **Email Headers**

Email headers are lines of metadata attached to an email and contain many useful string of information for analysts and investigators

2. **Email Body**

The email body is the main content of an email message that is visible to the recipient

It typically contents the message that the sender wants to convey, including text, images, links and any attachments

3. **Email Addresses**

Email addresses are unique identifier assigned to individual or organization and entity enabling them to send and receive email through email services. Email have 2 part.

_EX : bob.smith@example.com_

- Local Part(Mailbox) : bob.smith
- Domain Part : example.com
- .com : TLD(Top-Level Domain)

4. **Email Protocols**

5. **Mail Agents**

- _Mail Transfer Agent (MTA)_
  - Route and transfer email messages across mail servers
  - Determine appropriate route and relays
  - MTA is a software application or server that's responsible for routing and transferring email message between different mail servers. And so, when an email is sent, the MTA on the sender's mail server accepts the message, looks up the destination message and then determine the appropriate route to deliver the email to the recipients mail server.
  - So when an email is sent from one domain to another it might have to traverse through multiple MTA's over the internet in a relay before reaching it's final destination

- _Mail user Agent (MUA)_
  - Compose, send, receive and manage email messages
  - Gmail, Outlook, Yahoo, Thunderbird

- _Mail Delivery Agent (MDA)_
  - Accepting incoming email message from MTAs
  - Placing the email in the recipient's inbox

- _Mail Submission Agent (MSA)_

- _Mail Retrieval Agent (MRA)_
