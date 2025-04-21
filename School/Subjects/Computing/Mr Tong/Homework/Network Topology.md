[[Computing]]
#18/3/25
## Introduction to Networks

A network is a group of interconnected computing devices that share resources and communicate with each other. Networks fall into two broad categories:
- **Local Area Network (LAN):** Covers a small geographical area such as a home, school, or office.
- **Wide Area Network (WAN):** Covers a large geographical area, often consisting of multiple LANs connected via telecommunications.
A standalone computer that is not connected to any network does not benefit from network resources.
## Network Topologies
A **network topology** refers to the arrangement of devices (nodes) and how they communicate within a network. There are two types of topology:
- **Physical topology:** The actual physical layout of network devices.
- **Logical topology:** How data flows within the network, which may differ from the physical layout.
### Bus Topology
#### Definition
A **bus topology** is a network arrangement where all nodes are connected to a single central cable, known as the **backbone**.
#### Operation
- All nodes are connected along a central cable.
- Each end of the backbone has a **terminator** to prevent data reflection.
- Data is transmitted in one direction at a time.
- Uses **Carrier Sense Multiple Access with Collision Detection (CSMA/CD)** to manage data transmission.
#### Advantages
- Simple to set up and requires less cabling.
- Cost-effective for small networks.
- Works well for small LANs with limited devices.
#### Disadvantages
- If the central cable fails, the entire network fails.
- Limited cable length and number of devices.
- Performance degrades as traffic increases due to data collisions.

### Star Topology
#### Definition
A **star topology** is a network where all nodes are connected to a central device (hub or switch).
#### Operation
- Each device connects to a central **hub** or **switch**.
- A **switch** directs data specifically to the intended device.
- A **hub** broadcasts data to all connected devices.
#### Advantages
- If one node fails, it does not affect the rest of the network.
- High performance due to reduced data collisions.
- Easy to add or remove devices without affecting the network.

#### Disadvantages
- More expensive due to additional cabling and hardware.
- If the central hub or switch fails, the entire network goes down.

## MAC Addressing

Each networked device has a **Network Interface Card (NIC)**, which is assigned a unique **Media Access Control (MAC) address** during manufacturing.
- Example of a MAC address: **3B-84-D8-A3-5C-7F**.
- A **switch** maintains a table of MAC addresses to direct data efficiently to the correct device.

## 4. Physical vs Logical Topology
- **Physical topology** refers to how devices are **physically** connected.
- **Logical topology** describes how devices **communicate** over the network.
- A network physically wired in a **star topology** can function logically as a **bus network** by using bus protocols.
## 5. Summary

| Feature              | Bus Topology                                 | Star Topology                                                        |
| -------------------- | -------------------------------------------- | -------------------------------------------------------------------- |
| Cost                 | Low                                          | High (due to extra hardware)                                         |
| Failure impact       | Entire network fails if the backbone is down | Only the failed node is affected unless the central hub/switch fails |
| Performance          | Slows down as traffic increases              | High performance due to reduced collisions                           |
| Ease of installation | Simple to set up                             | More complex due to additional hardware                              |