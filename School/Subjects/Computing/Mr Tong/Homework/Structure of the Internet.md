[[Computing]]
#27/9/25
### The Internet

- The Internet = "Inter-connected Networks" → the largest public network in the world.
- The World Wide Web (WWW) is a collection of resources accessed via the Internet.
- The Internet can also transmit data without using the web (e.g., email, VoIP, file transfer).
---
### Structure of the Internet
- Works like a road network – data can be sent anywhere if the destination address is known.
- Backbone = the central, high-capacity data routes connecting major networks worldwide.
- Regional networks (often controlled by Internet Service Providers, ISPs) connect to the backbone.
- ISP (Internet Service Provider) provides end-user access to the Internet.
---
### Internet Addresses
- Every device needs a unique identifier (like a postal address).
- Uses the Internet Protocol (IP) system.

**IPv4**
- Made of four octets (8 bits each), written in decimal, e.g. `192.168.1.1`.
- Provides ~4.3 billion addresses, which is not enough for all devices.
**IPv6**
- Provides 128-bit addresses (~340 undecillion).
- Solves the address exhaustion problem.
---
### Domain Names and FQDN
- Domain Name = human-readable identifier (e.g., `bbc.co.uk`).
- Host Name = part of the domain identifying a server (e.g., `www.`).
- Fully Qualified Domain Name (FQDN) = complete name including host + domain (e.g., `www.bbc.co.uk`).
---
### Uniform Resource Locator (URL)

- Specifies how and where to access a resource.
- Structure:
    - Protocol → e.g., `http://`, `https://`
    - Domain name → e.g., `www.bbc.co.uk`
    - Resource path → e.g., `/index.html`
- Example: `http://www.bbc.co.uk/index.html`
---
### Domain Name System (DNS)
- DNS servers are directories mapping domain names to IP addresses.
- Process:
    1. User types a domain into a browser.
    2. Computer queries a DNS server.
    3. DNS server returns the corresponding IP address.
    4. Data can now be sent to that server.
- Why DNS? Easier than remembering IP addresses.
- Resolution: if a DNS server doesn’t know, it refers to higher-level DNS servers until resolved, or returns an error.
---
### Internet Registries
- IANA (Internet Assigned Numbers Authority) oversees global IP addresses and domain names.
- Responsibility is delegated to five Regional Internet Registries.
- Domain Registrars = organisations that sell domain names.
- Domain names must be unique, but the same name can exist with different Top-Level Domains (TLDs).
    - Example: `abcde.com` and `abcde.co.uk`