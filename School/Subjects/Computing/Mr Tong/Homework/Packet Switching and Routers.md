[[Computing]]
#1/10/25 
## Circuit Switching vs. Packet Switching

- **Circuit Switching**
    - Creates a dedicated communication link between two endpoints (like a traditional phone call).
    - Works well for single connections but not scalable for billions of devices on the Internet.
- **Packet Switching**
    - Data is split into **packets** and sent individually across shared network routes.
    - Packets may take **different routes** but are reassembled at the destination.
    - Allows efficient use of bandwidth since unused capacity can be shared.

---
## Data Packets

- A **packet** = payload (data) + **header** + **trailer**.
- **Payload**: the actual segment of data being transmitted (500–1500 bytes typical).
### Packet Header Includes:

- Recipient’s **IP address**.
- Sender’s **IP address**.
- **Packet number** & **total number of packets**.
- **Time To Live (TTL) / hop limit**.
### Packet Trailer Includes:
- **Error checking** information:
    - Checksums or Cyclical Redundancy Checks (CRC).
    - Ensures data has not been corrupted in transit.
    - If errors found → packet is resent.

---
## Example of Data Transfer
- Sending a **10 GB file** with packets of 1500 bytes:
    - 10,000,000,000 / 1,500 ≈ 6,666,667 packets needed.

---
## Packet Travel Across the Internet

- **Each packet** chooses the **fastest available route**.
- **Latency** = time for packet to travel:
    - London → Paris: ~5ms.
    - London → Sydney: ~40ms.
- **Packets are reordered** at the receiving device.

---
## Routers & Routing
- **Routers** forward packets between networks.
- Each router uses a **routing table** to decide where to send packets.
- Each step between routers = **a hop**.
- Process continues until the **destination node** is reached.

---

## 6. Gateways
- Needed when data travels between **different networks/protocols**.
- Functions:
    - Remove and reapply **headers** in correct format for the new network.
    - Can be integrated with routers.

---

## 7. Key Terms Recap

- **Packet switching** = breaking data into small packets sent independently.
    
- **Router** = forwards packets to correct destination across networks.
    
- **Hop** = each step a packet takes from one router to another.
    
- **Gateway** = device that allows communication between networks with different protocols.
    
- **Latency** = time taken for a packet to reach its destination.