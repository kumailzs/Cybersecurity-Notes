### 1. Basic Terms

- **IP (Internet Protocol)**  
  A set of rules that decides how data packets travel in a network.

- **IP Address**  
  A unique number given to a device so it can be identified on the network.

- **IP Addressing**  
  The system of assigning IP addresses to devices and also deciding the size of the network.

---

### 2. IPv4 vs IPv6

| Feature   | IPv4        | IPv6        |
| --------- | ----------- | ----------- |
| Bits      | 32 bits     | 128 bits    |
| Format    | 192.168.1.2 | 2001:db8::1 |
| Structure | 4 octets    | 8 groups    |

**Why do we say “bits”?**  
Computers only understand 0 and 1 (binary). An IPv4 address is made of 32 zeros and ones, so we call it a 32-bit address.

---

### 3. Octet and Byte

- 1 Bit = 0 or 1
- 8 Bits = 1 **Octet** = 1 **Byte**
- IPv4 has 4 Octets = 32 bits
- We write it in dotted decimal format so humans can read it easily.

---

### 4. Public vs Private IP

**Private IP Ranges:**
- 10.0.0.0 — 10.255.255.255
- 172.16.0.0 — 172.31.255.255
- 192.168.0.0 — 192.168.255.255

Any IP outside these ranges is a **Public IP**.

**Note:** 172.32.x.x is **not** private. It is public.

---

### 5. Network ID and Host ID

Every IP address is divided into two parts:

- **Network ID** → Identifies the whole network
- **Host ID** → Identifies a specific device inside that network

This division is decided by the **Subnet Mask**.

**Example:**
- IP: 192.168.1.2
- Mask: 255.255.255.0 (/24)
- Network ID = 192.168.1.0
- Host ID = 2

---

### 6. How Network ID and Host ID are Assigned

- **Network ID** → Set by the Router / Network Admin / ISP
- **Host ID** → 
  - Mostly given automatically by DHCP
  - Or set manually (Static IP)

---

### 7. Subnet Mask and CIDR

The Subnet Mask tells us how many bits are used for the Network and how many are used for the Host.

- 255.255.255.0 = /24
- 24 bits = Network
- 8 bits = Host

In **CIDR**, you can use any mask you want (/22, /25, /27, /30, etc.).  
In the old Classful system, the mask was fixed.

---

### 8. Calculating Number of Hosts

**Formula:**  
Usable Hosts = 2^(Host bits) – 2

| CIDR | Host bits | Usable Hosts |
|------|-----------|--------------|
| /24  | 8         | 254          |
| /25  | 7         | 126          |
| /26  | 6         | 62           |
| /30  | 2         | 2            |

---

### 9. Extra Points about Private and Public IP

- The Network + Host structure exists in **both** Private and Public IPs.
- Private IPs can be the same in many places because of **NAT**.
- Public IPs must be unique across the whole internet.
- Customers of the same ISP often share the same Network portion in their Public IP.

**NAT:** Converts Private IP into Public IP when the device goes to the internet.

---

### 10. IP Classes (Classful Addressing)

| Class | Range                          | Default Mask | Use                        |
|-------|--------------------------------|--------------|----------------------------|
| A     | 1.0.0.0 – 126.255.255.255     | /8           | Very large networks        |
| B     | 128.0.0.0 – 191.255.255.255   | /16          | Medium networks            |
| C     | 192.0.0.0 – 223.255.255.255   | /24          | Small networks             |
| D     | 224.0.0.0 – 239.255.255.255   | —            | Multicast                  |
| E     | 240.0.0.0 – 255.255.255.255   | —            | Experimental / Reserved    |

**Why were classes created?**  
To easily give different sized networks to different organizations.  
But the system was rigid and wasted many addresses, so CIDR was introduced.

---

### 11. Important Reality

IP Addressing is not only about giving an IP to a device.  
It also decides the **size of the network** using the Subnet Mask.

---

### 12. Real Example

- IP: 192.168.1.2
- Mask: 255.255.255.0 (/24)
- Network ID: 192.168.1.0
- Host ID: 2
- Gateway: 192.168.1.1
- Maximum usable hosts: 254

