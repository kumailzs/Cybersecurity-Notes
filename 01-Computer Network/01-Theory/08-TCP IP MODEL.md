The TCP/IP model is a four-layer framework used to describe how data is packetized, addressed, transmitted, and received over the internet. Its layers are the Application layer, Transport layer, Internet layer, and Network Access (Link) layer. When data transfer so it passed from layer 1(Application Layer) to layer 4(Physical Layer).h

![[Pasted image 20260920121619.png]]

## Protocols
### 1. Application Layer

This layer contains user-facing network services and protocols:

|Protocol|Function|
|---|---|
|**HTTP**|Transfers website data|
|**HTTPS**|Secure/encrypted HTTP|
|**DNS**|Converts domain names → IP addresses|
|**DHCP**|Automatically provides devices with IP/network settings|
|**FTP**|Transfers files|
|**SFTP**|Secure file transfer|
|**SSH**|Securely accesses a remote computer/server|
|**SMTP**|Sends emails|
|**POP3**|Receives/downloads emails|
|**IMAP**|Manages/synchronizes emails with the mail server|

---

### 2. Transport Layer

| Protocol | Function                                                           |
| -------- | ------------------------------------------------------------------ |
| **TCP**  | Reliable delivery using ACKs, sequence numbers, and retransmission |
| **UDP**  | Fast/simple delivery without TCP-style reliability                 

**Example:**

Browser → HTTPS → **TCP** → IP → Ethernet/Wi-Fi

---
### 3. Internet Layer

| Protocol           | Function                                               |
| ------------------ | ------------------------------------------------------ |
| **IP (IPv4/IPv6)** | Addressing and routing packets across networks         |
| **ICMP**           | Network diagnostics and error reporting — e.g., `ping` |
| **IGMP**           | IPv4 multicast group management                        |

---
### 4. Network Access Layer

This layer handles actual **frame transmission over the local network**:

| Protocol/Technology  | Function                                                |
| -------------------- | ------------------------------------------------------- |
| **Ethernet (802.3)** | Wired LAN communication                                 |
| **Wi-Fi (802.11)**   | Wireless LAN communication                              |
| **ARP**              | Finds the corresponding MAC address for an IPv4 address |