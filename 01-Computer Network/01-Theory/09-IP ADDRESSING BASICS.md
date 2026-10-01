# Basic Terms

- **IP (Internet Protocol)**  
    A set of rules that decides how data packets travel in a network.
    
- **IP Address**  
    A unique number given to a device so it can be identified on the network.
    
- **IP Addressing**  
    The system of assigning IP addresses to devices and also deciding the size of the network.


---

## IPv4 vs IPv6

|Feature|IPv4|IPv6|
|---|---|---|
|Bits|32 bits|128 bits|
|Format|192.168.1.2|2001:db8::1|
|Structure|4 octets|8 groups|

**Pasted image 20261001020815.png**

**Why do we say “bits”?**  
Computers only understand 0 and 1 (binary). An IPv4 address is made of 32 zeros and ones, so we call it a 32-bit address.

---

## Octet and Byte

- 1 Bit = 0 or 1
    
- 8 Bits = 1 **Octet** = 1 **Byte**
    
- IPv4 has 4 Octets = 32 bits
    
- We write it in dotted decimal format so humans can read it easily.

---

## Public vs Private IP

**Private IP Ranges:**

- 10.0.0.0 — 10.255.255.255
    
- 172.16.0.0 — 172.31.255.255
    
- 192.168.0.0 — 192.168.255.255

Any IP outside these ranges is a **Public IP**.

**Note:** 172.32.x.x is **not** private. It is public.

---

## Network ID and Host ID

Every IP address is divided into two parts:

- **Network ID** → Identifies the whole network
    
- **Host ID** → Identifies a specific device inside that network

This division is decided by the **Subnet Mask**.

**Example:**

- IP: 192.168.100.10
    
- Mask: 255.255.255.0 (/24)
    
- Network ID = 192.168.100.0
    
- Host ID = 10

**Pasted image 20261001020709.png**

---

## How Network ID and Host ID are Assigned

- **Network ID** → Set by the Router / Network Admin / ISP
    
- **Host ID** →
    
    - Mostly given automatically by DHCP
        
    - Or set manually (Static IP)
        

---

## Subnet Mask and CIDR

The Subnet Mask tells us how many bits are used for the Network and how many are used for the Host.

- 255.255.255.0 = /24
    
- 24 bits = Network
    
- 8 bits = Host
    

In **CIDR**, you can use any mask you want (/22, /25, /27, /30, etc.).  
In the old Classful system, the mask was fixed.

---

## Calculating Number of Hosts

**Formula:**  
Usable Hosts = 2^(Host bits) – 2

|CIDR|Host bits|Usable Hosts|
|---|---|---|
|/24|8|254|
|/25|7|126|
|/26|6|62|
|/30|2|2|

---

## Extra Points about Private and Public IP

- The Network + Host structure exists in **both** Private and Public IPs.
    
- Private IPs can be the same in many places because of **NAT**.
    
- Public IPs must be unique across the whole internet.
    
- Customers of the same ISP often share the same Network portion in their Public IP.
    

**NAT:** Converts Private IP into Public IP when the device goes to the internet.

---

## Important Reality

IP Addressing is not only about giving an IP to a device.  
It also decides the **size of the network** using the Subnet Mask.

---

# Classical Addressing

- **Classful Addressing:** To distribute IP addresses based on organizational needs, IPv4 was originally divided into 5 classes: **Class A, B, C, D, and E**.
    
- **IPv4 Address Size:** An IPv4 address consists of **32 bits** divided into **4 octets** (8 bits each), represented in dotted-decimal format (e.g., `W.X.Y.Z`).

---

## Class A (For Very Large Networks)

- **Target Use:** Designed for massive organizations requiring millions of connected devices across a small number of networks.
    
- **Address Division:** `Network ID (8 bits) | Host ID (24 bits)`
    
- **First Octet Fixed Bits:** The first bit is always fixed to `0` (`0xxxxxxx`).
    
- **First Octet Decimal Range:** `**0**` **to** `**127**` (e.g., `10.0.0.1`).
    
- **Total Usable Networks:** 2^7 - 2 = 126 (`0.0.0.0` and `127.x.x.x` are reserved).
    
- **Usable Hosts per Network:** 2^{24} - 2 = 16,777,214.
    
- **Default Subnet Mask:** `255.0.0.0`
    

---

## Class B (For Medium to Large Networks)

- **Target Use:** Designed for medium-to-large organizations, such as universities or large corporations.
    
- **Address Division:** `Network ID (16 bits) | Host ID (16 bits)`
    
- **First Octet Fixed Bits:** The first two bits are always fixed to `10` (`10xxxxxx`).
    
- **First Octet Decimal Range:** `**128**` **to** `**191**` (e.g., `172.16.0.1`).
    
- **Total Usable Networks:** 2^{14} = 16,384.
    
- **Usable Hosts per Network:** 2^{16} - 2 = 65,534.
    
- **Default Subnet Mask:** `255.255.0.0`
    

---

## Class C (For Small Networks)

- **Target Use:** Designed for small businesses, local area networks (LANs), or home networks needing fewer connected devices.
    
- **Address Division:** `Network ID (24 bits) | Host ID (8 bits)`
    
- **First Octet Fixed Bits:** The first three bits are always fixed to `110` (`110xxxxx`).
    
- **First Octet Decimal Range:** `**192**` **to** `**223**` (e.g., `192.168.1.5`).
    
- **Total Usable Networks:** 2^{21} = 2,097,152.
    
- **Usable Hosts per Network:** 2^8 - 2 = 254.
    
- **Default Subnet Mask:** `255.255.255.0`
    

---

## Class D (For Multicasting)

- **Target Use:** Reserved exclusively for **Multicasting** (group communication, video streaming, routing protocol updates). It cannot be assigned to individual end-user devices.
    
- **Address Division:** No division between Network ID and Host ID.
    
- **First Octet Fixed Bits:** The first four bits are always fixed to `1110` (`1110xxxx`).
    
- **First Octet Decimal Range:** `**224**` **to** `**239**` (e.g., `224.0.0.5`).
    
- **Total IP Addresses:** 2^{28} (approx. 250 million addresses).
    
- **Default Subnet Mask:** Not Applicable
    

---

## Class E (For Experimental & Military Use)

- **Target Use:** Reserved for **Research, Development (R&D), and Military purposes**. Not available for general public or commercial internet use.
    
- **Address Division:** No division between Network ID and Host ID.
    
- **First Octet Fixed Bits:** The first four bits are always fixed to `1111` (`1111xxxx`).
    
- **First Octet Decimal Range:** `**240**` **to** `**255**` (e.g., `245.1.1.1`).
    
- **Total IP Addresses:** 2^{28} (approx. 250 million addresses).
    
- **Default Subnet Mask:** Not Applicable
    

---

## Key Rule: Why Subtract 2 ("Minus 2 Rule")?

When calculating usable host addresses in any network, **2** addresses are subtracted from the total because they serve dedicated operational functions:

1. **Network Address (All host bits set to** `**0**`**):** Identifies the network itself (e.g., `192.168.1.0`).
2. **Direct Broadcast Address (All host bits set to** `**1**`**):** Used to send packets to all host devices on that specific network simultaneously (e.g., `192.168.1.255`).

Neither of these two addresses can be assigned to individual computer interfaces.

# Classless Addressing (CIDR)

![[Pasted image 20261001231637.png]]
## Overview & Why CIDR?

- **Problem with Classful Addressing:** Fixed IP classes (A, B, and C) caused massive IP address wastage. For example, an organization needing 1,000 IPs could not use Class C (254 IPs) and was forced to take Class B (65,536 IPs), wasting over 64,000 addresses.
- **The Solution:** In 1993, **Classless Inter-Domain Routing (CIDR)** was introduced to replace rigid classes.
- **Block Allocation:** Instead of fixed classes, IP addresses are allocated in customized **Blocks** based on exact user requirements (managed by IANA).
## CIDR Notation (Slash Notation)
- **Format:** `x.y.z.w / n`
- **Meaning of `/n`:** The `/n` prefix represents the number of **Network bits** (or continuous 1s in the subnet mask).
- **Host Bits Formula:** $\text{Host Bits} = 32 - n$
- **Total Addresses Formula:** $\text{Total IPs in Block} = 2^{(32 - n)}$
## Step-by-Step Example: `200.10.20.40 / 28`

- **Network Bits ($n$):** 28 bits
- **Host Bits:** $32 - 28 = 4$ bits
- **Total IPs in Block:** $2^4 = 16$ addresses
- **Subnet Mask:** 28 binary ones followed by 4 binary zeros:
`11111111 . 11111111 . 11111111 . 11110000` = `255.255.255.240`

### Finding the Network ID (Block ID):

1. The first 3 octets (24 bits) remain unchanged: `200.10.20`.
2. Convert the 4th octet (`40`) into 8-bit binary: `00101000`.
3. Since $n = 28$, the first 4 bits belong to the Network (`0010`) and the last 4 bits belong to the Host (`1000`).
4. Set all Host bits to `0`: `00100000` = `32` in decimal.
5. **Network ID:** **`200.10.20.32 / 28`**
## Three Golden Rules of CIDR Blocks

A CIDR block is valid only if it satisfies all three rules:

1. **Contiguous IPs:** All IP addresses in a block must be in continuous sequential order without any gaps.
2. **Power of 2:** The total number of IP addresses in a block must be a power of 2 (e.g., $2^1=2$, $2^2=4$, $2^3=8$, $2^4=16$). Block sizes cannot be odd or non-power numbers like 17 or 50.
3. **Divisibility Rule:** The first address of the block (Network ID) must be evenly divisible by the total size of the block. 
- **Shortcut:** If the block size is $2^k$, the last $k$ bits in the binary representation of the Network ID must all be `0`.