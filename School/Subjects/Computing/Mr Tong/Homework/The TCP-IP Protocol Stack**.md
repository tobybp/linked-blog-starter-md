[[Computing]]
#8/11/25

- Purpose:  
The **TCP/IP stack** is a set of rules (protocols) that govern how data is transmitted across networks like the Internet.  
It breaks network communication into **four layers**, each with a specific role.

|Layer|Name|Description|Example Protocols|
|---|---|---|---|
|1|**Application Layer**|Provides services and standards for communication between software applications.|HTTP, FTP, SMTP, IMAP|
|2|**Transport Layer**|Establishes end-to-end connections, splits data into packets, ensures reliable delivery.|TCP, UDP|
|3|**Internet Layer**|Handles addressing and routing of packets between networks.|IP (Internet Protocol)|
|4|**Link Layer**|Operates across the physical connection; manages MAC addressing and hardware transmission.|Ethernet, Wi-Fi|

**Mnemonic:** 🧩 _Apple Tango Is Lush_  
(Application, Transport, Internet, Link)

---
### **Data Transmission Through Layers**
#### **Sending Data:**
1. **Application Layer** – Formats the data (e.g., HTTP request for a webpage).
2. **Transport Layer** – Splits data into packets, numbers them, and adds **port numbers** (e.g., port 80 for HTTP).
3. **Internet Layer** – Adds **IP addresses** for source and destination.
4. **Link Layer** – Adds **MAC addresses** for delivery across the physical network.
#### **Receiving Data:**
The process is reversed — each layer strips off its header and passes data up the stack until the original message is reconstructed.

---
### **MAC and IP Addresses**

|Type|Description|Example|
|---|---|---|
|**IP Address**|Logical address used to identify a device on a network.|192.168.1.10|
|**MAC Address**|Physical hardware address of a NIC (Network Interface Card).|4B:24:A2:73:0E:F1|

- **IP addresses remain constant** across the route.
- **MAC addresses change** at each router hop.
- Each router uses the **next hop MAC address** to forward packets.

---
### **Port Numbers & Sockets**

- A **port number** identifies a specific service or process on a computer.
- A **socket** = IP address + Port number (e.g., `42.205.110.140:80`)    

**Common Ports:**

|Protocol|Function|Port|
|---|---|---|
|HTTP|Web browsing|80|
|HTTPS|Secure web|443|
|FTP|File transfer|20, 21|
|SSH|Secure Shell|22|
|SMTP|Send email|25|
|POP3|Retrieve email (downloads)|110|
|IMAP|Retrieve email (syncs)|143|

---
### **FTP (File Transfer Protocol)**
- Used to **transfer files** across a network.
- Operates via **client–server model**.
- Uses:
    - **Port 20** – Data transfer
    - **Port 21** – Command/control
- Can be **anonymous** or **authenticated** (using username/password).

---
### **SSH (Secure Shell)**
- Used for **secure remote management** of computers and servers.
- Uses **encryption** (public/private keys) to protect data from eavesdropping.
- **Port 22** by default.
- Can create **SSH tunnels** to securely pass blocked or sensitive data.

---
### **Email Protocols**

|Protocol|Function|Port|Key Feature|
|---|---|---|---|
|**SMTP**|Sending and forwarding email between servers|25|Sends email out|
|**POP3**|Downloads and removes email from server|110|Offline storage|
|**IMAP**|Keeps mail on server, syncs across devices|143|Multi-device access|

- If emails read on one device don’t appear on another → POP3 is being used.

---

### ** Web Technologies**
- **Web pages** are built with **HTML**, **CSS**, and **JavaScript**.
- **Web servers** host sites and deliver pages to clients.
- **Web browsers** request pages (via HTTP/HTTPS), interpret HTML/CSS/JS, and render the output.

---
### **Why Layers Are Important**

- **Modularity:** Each layer performs a specific function independently.
- **Abstraction:** Higher layers don’t need to know how lower layers work.
- **Flexibility:** Layers can be updated without affecting others.
- **Troubleshooting:** Problems can be isolated by layer.

---
### **Example: Transmitting a Web Page**
**Scenario:** A company’s internal HTML page is transmitted over Ethernet using TCP/IP.
1. **Application Layer:**
    - HTTP formats and requests the webpage from the server.
2. **Transport Layer:**
    - TCP splits the webpage into packets, adds port 80 (HTTP).
3. **Internet Layer:**
    - Adds the IP address of the destination web server.
4. **Link Layer:**
    - Adds MAC address for next device (e.g., router).