# Day 1

## OSI Model

| Layer Index | Layer Name         | Work                             |
| ----------- | ------------------ | -------------------------------- |
| 7           | Application Layer  | Data                             |
| 6           | Presentation Layer | Data                             |
| 5           | Session Layer      | Data                             |
| 4           | Transport Layer    | Data + Layer 4 Header => Segment |
| 3           | Network Layer      | Data + Layer 4,3 => Packets      |
| 2           | Data Link Layer    | Data + Layer 4,3,2 => Frame      |
| 1           | Physical Layer     | Bits                             |

---

- **_In WireShark_**
  - **Ethernet II** is layer 2 Protocol _(Data Link Layer)_
  - **Internet Protocol Version** is a layer 3 Protocol _(Network Layer)_
  - **User DataGram Protocol** is a layer 4 Protocol _(Transport Layer)_

- So only there are 2 transport inlayer 4 One is TCP and One is UDP

---

- **_In WireShark_**
  - _L2 : Ethernet II_
    - Destination mac Address, Sources Mac Address
  - _L3 : Internet Protocol (IP)_
    - Sources IP, Destination IP, TTL(Time To Live), IP options, Ip identifier, ICMP Quotes .
  - _L4 : 4 Tuple Connection_
    - Sources Ip, Sources Port, Destination IP, Destination Port
    - TCP Options, Retransmissions, Windows Scaling, Explicit Congestion Notification (ECN)

---

- **_TTL = Time to Live_**

It will come from Destination to the Sources

```bash
$ ping <ip>
$ tracert <ip>
```

| OS            | TTL |
| ------------- | --- |
| Windows       | 128 |
| Linux         | 64  |
| Cisco Devices | 255 |

---

# Day 2
