## IP Address ( Internet Protocol Address )

![Computer Network](../../attachments/Pasted%20image%2020261012104516.png)
- **Layer :** Network Layer
- **What's this :** Every nodes (device like mobile phones, routers, laptops, server etc) connected in a network that has its unique identifier number that's called IP Address.
- **Who's Assign :** It's assign by our adminstator, router and ISP.
- **Length / Format :**
1. **IPV4 :** It's 32 bits IP Address represented in dotted decimal e.g 192.168.1.1.
2. **IPV6 :** It's 128 bits IP Address represented in hexadecimal e.g 2345:0425:2CA1:0000:0000:0567:5673:23b5
- **What's Use :** It's use for Gobal internet routing (to deciide path to travel data packet from source to destination). It's also use to travel data packet from source to destination.
- **Property :** When data packet travel from source to destination in internet so, ip address is always same (unchanged).
- **Network Device :** Router use IP Address to foward data packet into internet.
## MAC Address ( Media Access Control Address)

![Computer Network](../../attachments/Pasted%20image%2020261012020235.png)
- **Layer :** Data-Link Layer
- **What's this :** MAC Address is the unique identifier assigned to NIC (Network Interface Card).
- **Who's Assign :** It's assign by manufacture company (like intel, reltek, and etc).
- **Length / Format :** It's 48 bits and represented in hexadecimal with colon or hyphen e.g 00:1A:2B:3C:4D:5E
- **What's Use :** It's only use for communication between nodes in a LAN.
- **Property :** When physical frame hop (travel one router to another router) so, MAC Address is change in every hop.
- **Network Device :** Switch/NIC use MAC Address to foward physical frame into network.
## Port Address ( Port Number )

![Computer Network](../../attachments/Pasted%20image%2020261012105030.png)
- **Layer :** Transport Layer
- **What's this :** Port Number is unique address of a process of a services in a computer.
- **Lenth / Format :** It's 16 bits and it's range is 0 to 65535.
- **What's Use :** In our computer multiple services running like you watching a video in Youtube, download something, Whatsapp, etc. so, how identify which data segment is for which application or service so, port address identify which data segment is for which service.
- **Famous Port Examples :**
1. **Port 80:** HTTP (Normal web traffic)
2. **Port 443:** HTTPS (Secure web traffic)
3. **Port 21:** FTP (File Transfer)
4. **Port 25:** SMTP (Email)

## 📊 Quick Comparison Table

| **Feature**                 | **MAC Address**                | **IP Address**                             | **Port Address**                 |
| --------------------------- | ------------------------------ | ------------------------------------------ | -------------------------------- |
| **Layer**                   | Data Link Layer (Layer 2)      | Network Layer (Layer 3)                    | Transport Layer (Layer 4)        |
| **Type**                    | Physical / Hardware            | Logical                                    | Process / Application Identifier |
| **Length**                  | 48-bit (Hexadecimal)           | 32-bit (IPv4) / 128-bit (IPv6)             | 16-bit (0 to 65535)              |
| **Scope**                   | Local Network (LAN)            | Global / End-to-End                        | Inside the Host Machine          |
| **Changes during routing?** | **Yes** (It changes every hop) | **No** (Source to Destination always same) | **No**                           |
| **Managed by**              | Manufacturer (Permanent)       | ISP / Network Admin / DHCP                 | Operating System / Application   |

---

## Related Notes
- [Logical vs Physical Addressing](10-%20Logical%20Addressing%20Vs%20Physical%20Addressing.md)
- [OSI Model](07-OSI%20MODEL.md)

## References
- [RFC 791 – Internet Protocol (IPv4)](https://www.rfc-editor.org/rfc/rfc791)
- [IANA – Service Name and Transport Protocol Port Number Registry](https://www.iana.org/assignments/service-names-port-numbers/service-names-port-numbers.xhtml)

---

[← Previous](08-TCP%20IP%20MODEL.md) | [Contents](../../README.md) | [Next →](10-%20Logical%20Addressing%20Vs%20Physical%20Addressing.md)