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



# Classless Addressing (CIDR):

## 1. What is an IP address?

An IP address is a line of 32 bits (0s and 1s). We usually see it written with dots:

```
200      .  10       .  20       .  32
11001000 . 00001010 . 00010100 . 00100000
```

This line has two parts:

- **Network part** (first bits): which network
- **Host part** (remaining bits): which device inside that network

## 2. Problem with classful addressing

The boundary between network and host was fixed (only 8, 16, or 24 bits). So there were only 3 block sizes:

|Class|Addresses|
|---|---|
|A|about 16.7 million|
|B|65,536|
|C|256|

If an organization needed 1,000 IPs, Class C was too small and Class B was too big. **Over 64,000 addresses were wasted.**

## 3. What is CIDR?

CIDR (Classless Inter-Domain Routing) was introduced in 1993. The boundary is no longer fixed. It can be anywhere, so the block size matches what the user needs. Blocks are managed by IANA.

Example: for 1,000 IPs you get a `/22` (1,024 addresses), so very little is wasted.

## 4. What is a block?

**A block is the range of all IP addresses of one network.** All addresses in a block share the same network part.

## 5. CIDR notation: `x.y.z.w/n`

`/n` means: **the first n bits of the 32 are network bits.**

```
Host bits       = 32 − n
Total addresses = 2^(host bits)
Usable host IPs = total − 2
```

**Remember:** the bigger `n` is, the smaller the block.

|Prefix|Host bits|Total addresses|Usable host IPs|
|---|---|---|---|
|/30|2|4|2|
|/29|3|8|6|
|/28|4|16|14|

Why subtract 2?

- **First address** = Network ID (the name of the network)
- **Last address** = Broadcast (message to all devices)

Neither can be given to a device.

## 6. Example: `200.10.20.40/28`

**Basic info**

- Network bits = 28
- Host bits = 32 − 28 = 4
- Total addresses = 2⁴ = 16
- Subnet mask = 28 ones followed by 4 zeros:  
    `11111111.11111111.11111111.11110000` = **255.255.255.240**

**Finding the Network ID**

1. The first 3 octets stay the same: `200.10.20`
2. Write the 4th octet `40` in binary: `0010 1000`
3. First 4 bits are network (`0010`), last 4 bits are host (`1000`)
4. Set the host bits to 0: `0010 0000` = 32
5. **Network ID = 200.10.20.32/28**

**Other values**

- Broadcast: set all host bits to 1, `0010 1111` = 47
- Block range: `.32` to `.47`
- Usable host IPs: `.33` to `.46` (14 devices)

Note: `.40` is just one address inside the block. It is not the start of the block.

## 7. Three rules for a valid CIDR block

**Rule 1: Contiguous.** Addresses must be in a continuous sequence with no gaps.

**Rule 2: Power of 2.** Block size can only be 2, 4, 8, 16, 32... never 17 or 50, because host bit combinations are always a power of 2.

**Rule 3: Divisibility.** The first address (Network ID) must be divisible by the block size.

**Shortcut:** if the size is 2ᵏ, the last k bits of the Network ID must all be 0.

Why? Because the first address of a block always has all host bits set to 0:

- `200.10.20.32` is valid (32 ÷ 16 = 2, binary `0010 0000`, last 4 bits are 0)
- A 16-address block cannot start at `200.10.20.40` (40 ÷ 16 = 2.5, binary `0010 1000`, last 4 bits are not 0)
