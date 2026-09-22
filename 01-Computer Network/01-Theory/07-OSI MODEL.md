OSI Model (Open System Interconnected Model) is the references model that is used to understand how data travels from one device to another. It divide networking process into 7 different layers and each layer have different function, protocols.

![[Pasted image 20260919145554.png]]
## Layer 7 (Application Layer)
it's software based layer and it works on application. It handle the interaction between user and network.
**Protocols** :
- **HTTP / HTTPS** (Web browsing / secure web)
- **FTP** (File Transfer Protocol)
- **SMTP** (Simple Mail Transfer Protocol - Outlook/Email)
- **DNS** (Domain Name System)
- **Telnet / RDP** (Remote Desktop)
**For Example**
When you search something on google so application layers work on there.

## Layer 6 (Presentation Layer)
it prepares data in proper form.
- Convert ASCII/Unicode into binary.
- Compressed large data/file.
- Encryption, SSH (When data is sensitive like passwords, personal info and etc).
## Layer 5 (Session Layer)
It established, maintained, managed and terminated session
- Authentication (match the login credential).
- Authorized (check the user is allow to access specific data).
## Layer 4 (Transport Layer)
it create end to end communication and reliability.
- Segmentation (It break data into small segments(pieces)).
- Flow Control (match the transmitter and reciever speed).
- Error Control (use ARQ to restore loss packet and checksum for error detection).
## Layer 3 (Network Layer)
it handle logical addressing and routing
- It form packet (by add source and destination ip address on segment)
- It finding best path for travel packet.
## Layer 2 (Data Link Layer)
It handle physical addressing and media access.
- It convert segment into frames (by adding source and destination MAC address and tail (it's use to detect error))
- MAC Address Types : Ethernet, Wifi and Fiber Optics have different MAC Address.
- It used Media Access Control to avoid collision.
### Layer 1 (Physical Layer)
It convert bits into actual physical signals.
**Media & Signals:**
- **Copper wire (Ethernet):** Electrical square wave signals (0s aur 1s).
- **Optical fiber:** Light signals (laser diode ON/OFF).
- **Wireless (4G/5G/Wi-Fi):** Electromagnetic waves.

### Protocols
A protocol is a set of rules that determines how data is sent and received over a network. The protocol is just like a language that computers use to talk to each other, ensuring they understand and can respond to each other's messages correctly. Protocols help make sure that data moves smoothly and securely between devices on a network.
### Encapsulation
It's process when data send from one device to another so data passed from layer 7 to layer 1 and each layer add there own header is called escapsulation.
### Decapsulation
It's also process when data reached to receiver so it passed from layer 1 to layer 7 is called decapsulation.