[[Computing]]
#17/10/25 
### Firewalls
**Definition:**  
A firewall is _software or hardware_ that controls access to and from a network.
#### Functions:
- Monitors data packets entering or leaving a network.
- Blocks or allows traffic based on predetermined rules.
- Uses **ports** (numbered doors) to manage specific network services (e.g. HTTP → port 80).
#### Types of Firewalls:
- **Packet Filtering:**  
    Inspects packet headers (source/destination IP and port numbers). Blocks packets not matching rules.  
    - Example: Block all ports except 80 and 443 for web traffic.  
    - Ports are **not left open** by default to prevent unauthorized access.
- **Stateful Inspection:**  
    Examines packet payloads and tracks ongoing “conversations” between computers.  
    Only allows returning data if it matches an existing, valid session.
- **Proxy Servers:**  
    Acts _on behalf of_ a client to access the internet.  
    Benefits:
    - Hides user’s real IP (anonymous browsing).
    - Filters content (e.g. parental or corporate controls).
    - Logs user activity.
    
    - Caches websites for faster access.
        

---

### 🔐 2. Encryption

**Definition:**  
Encryption converts **plaintext** into **ciphertext** using a **key**, making it unreadable without the key.

#### 🔸 Symmetric Encryption

- Same key used for **encryption and decryption**.
    
- **Fast**, but requires secure **key exchange**.
    
- Vulnerable to “man-in-the-middle” attacks if key is intercepted.
    
- Used in **Wi-Fi (PSK)** and **bulk data transfer**.
    

#### 🔸 Asymmetric Encryption

- Uses **two related keys**:
    
    - **Public key** (shared openly)
        
    - **Private key** (kept secret)
        
- One key encrypts, the other decrypts.
    
- Used in **TLS/HTTPS** to securely exchange a symmetric key.
    
- Slower, so often used only at the start of a secure session (hybrid encryption).
    

---

### ✍️ 3. Digital Signatures

Used to **verify authenticity and integrity** of a message.

**Process:**

1. Sender hashes the plaintext message.
    
2. Encrypts the hash using their **private key** (creates signature).
    
3. Sends the message + digital signature (often encrypted with recipient’s public key).
    

**Recipient:**

1. Decrypts the bundle using their **private key**.
    
2. Uses sender’s **public key** to decrypt the signature.
    
3. Hashes the received message.
    
4. Compares hashes — if they match, message is genuine and unaltered.
    

---

### 📜 4. Digital Certificates

- Prove the **identity** of a sender or website.
    
- Issued by **Certificate Authorities (CA)** like DigiCert, Let’s Encrypt.
    

**A certificate includes:**

- Serial number
    
- CA name
    
- Expiry date
    
- Subject (owner)
    
- Owner’s public key
    
- CA’s digital signature
    

**Used in:** HTTPS, email encryption, software signing.

---

### 🦠 5. Malware & Threats

#### 🧬 Virus

- Infects other files or programs.
    
- Needs user action to spread (e.g., opening an infected attachment).
    

#### 🐛 Worm

- Standalone program that self-replicates.
    
- Exploits system vulnerabilities.
    
- Spreads automatically without user action.
    

#### 🎭 Trojan

- Malicious software disguised as legitimate.
    
- Cannot self-replicate.
    
- Often opens **backdoors** for attackers to access the system remotely.
    

#### 📧 Phishing

- Uses fake emails/websites to trick users into revealing personal data.
    
- Targets less-aware users.
    
- Consequences: identity theft, fraud.
    

---

### 💻 6. Improving Code Quality and Protection

**Good practices:**

- Guard against **buffer overflow attacks**  
    → Prevents overwriting adjacent memory locations.
    
- Guard against **SQL injection**  
    → Always validate and sanitize user inputs.  
    Example:
    
    `SELECT * FROM Customers WHERE CustID = '21104710'; DROP TABLE Accounts;`
    
- Use:
    
    - **Strong passwords**
        
    - **Two-factor authentication**
        
    - **Access control / file permissions**
        

---

### 📊 7. Monitoring & Protection

**Monitoring Tools:**

- **Packet sniffers:** Detect unauthorized traffic.
    
- **User access logs:** Track logins and activity.
    

**Protection Measures:**

- Keep OS and applications **patched**.
    
- Use **up-to-date anti-malware** software.
    
- Regularly back up important data.