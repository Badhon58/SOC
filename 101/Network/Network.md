# Network Security

## Network Layer Protocols

- **_Internet Protocol(IP)_**
  - Ip Addressing
  - Ip routing

- **_Transmission Control Protocol(TCP)_**
  - Connection-oriented-reliable
  - Three way Handshake
  - Flow and congestion control

- **_User DataGram Protocol_**
  - Connection less
  - Lightweight, low-overhead-speed over reliability
  - VoIP, video streaming, audio streaming

---

## Packet Capture (PCAP)

- **Intercepting Packets**
  - Port mirroring (SPAN Ports)
  - Inline network devices
  - Network taps

- **PCAP Files**
  - Binary file format
  - Header and raw payload
  - Tcpdump, WireShark, Tsharks, etc.

- **Advantages**
  - Most detailed record
  - includes packets payload

- **Disadvantages**
  - Resource intensive
  - Requires significant storage space
  - Hard to scale

- **Aggregated metadata**

- **5-Tuple**
  - Source IP
  - Source Port
  - Destination IP
  - Destination Port
  - Transport Protocol

- **Advantages**
  - Efficient bandwidth and storage requirements
  - High level pattern and anomaly detection
  - Easier to scale

- **Disadvantages**
  - Lacks payload detail
  - Doesn't give you the whole picture
