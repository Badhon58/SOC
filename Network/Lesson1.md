# Networking Fundamentals

## A

**_Network Devices_**

- _Hosts_
  - Hosts are any device which sends or receive traffic : Computer, Laptop, Phones, Printers, Servers, Cloud Server
  - Also any Internet of Things (IOT) devices
    - TV, Thermometers, Speakers, Lights, Smart Watches, Refrigerator
  - Anythings that sends or receive traffic over a network

- _Client's and Servers_
  - Clients initiate requests, Servers responds
    - Relative to Specific Communication
  - Servers are simple computers with software installed which responds to specific requests

**_IP Address_**

- An IP Address is the identity of each host
- IP addresses are 32 bits
  - Bit = 1 or 0
  - Represented as four Octets
  - The smallest binary number we can get with 8 bit is 0. And the largest binary number we can get is 256
- Hierarchically Assigned

**_Networking_**

- A Network is what transports traffic between Hosts
  - Anytime two hosts are connected, you have a network
    - Before Networking
      - Transferring data between hosts required portable media
      - Disk, thumb drives
  - Logical grouping of hosts which require similar connectivity
  - Networks can contain other networks
    - Sometimes called Sub-Networks or Subnets
    - All those network is connected is a central resources namely Internet

**_Keys Take Ways_**

- Hosts are any device which sends or receive traffic
  - Client and Servers
- An IP Address is the identity if each host
- A network is what transports traffic between Hosts
  - Logical grouping of hosts which require similar connectivity
  - Sub networking, Subnets

## B

**_Repeater_**

- Data crossing a wire decays as it travels
- Repeaters regenerate signals
  - Allow communications across greater distances

- _Connecting hosts directly to each other doesn't scale_

**_Hub_**

- Hubs are simply multi-port Repeaters
  - Facilitates scaling communication between additional hosts
  - Everyone receives everyone else's data

**_Bridge_**

- Bridges sit between Hub-connected hosts
  - Bridges only have two ports
  - Bridges learn which hosts are on each side

**_Switch_**

- Switches facilitate communication **within** a network
- Switches are a combination of Hobs and Bridges
  - Multiple Ports
  - Learns which hosts are on each port
- _Network_ : Grouping of hosts which require similar connectivity
- Hosts on a network share the name IP address space

**_Router_**

- Routers facilitate communication between networks
  - _Network_ : Grouping of hosts which require similar connectivity
  - Provides a traffic control point (security, Filtering, Redirecting)
    - Traditionally, Switches could not perform such filtering
  - Routers learn which networks they are attached to
    - Known as Routers - Stored in a Routing Table
  - _Routing Table_ - all networks a Router knows about
  - Have IP addresses in the Networks they are attached to
  - Gateway each host's way out of their local Network

**_Keys Take Ways_**

- Routers facilitate communication between networks
- Switches facilitate communication within a network
- Routing is the process of moving data between networks
  - A Router is a device whose primary purpose is Routing
- Switching is the process of moving data within networks
  - A Switch is a device who's primary purpose is Switching
- **There are many other Network Devices**:
  - Access Points, Layer 3 Switches, Firewalls, IDS/IPS, Load Balancers, Proxies, Virtual Switches, Virtual Routers
- All of them perform Routing and/or Switching
