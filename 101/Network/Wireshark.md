## WireShark

- **What is WireShark**
  - WireShark is used for packet capture and analysis
  - Performs a lot of binary to English Translation
  - Deep protocol decoding capabilities
  - Lots of statistics and graphs

- **Format**
  - Hands-on Examples
  - Real-life captures

- ip.addr =

- _Protocol Filter_ I
  - Insert this in search bar
    - tcp
    - udp
    - undp
    - http

- _Address Filters_
  - ip.addr == 192.168.10.45
  - ip.addr == <mac-addr>
  - ip.addr == ff.ff.ff.ff.ff

- _Port Filters_
  - tcp.port == 80
  - udp.port == 53

- Logical Operators
  - "add (&&)", "or (||)", "not(!)"
  - tcp.port == 80 and ip.addr == <ip>
  - tcp.port == 443 or tcp.port == 80
  - not ip.addr == 192.168.30.20

---

_Profile_ : Change the Profile will store the data like a different user

---

**WireShark Statistics**

---

# NEW

TLS Secrets
Inject TLS Secrets
Inject ESP Secrets
