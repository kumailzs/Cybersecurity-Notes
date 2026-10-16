# IPv4 Address

## What is an IP Address?

An **IP (Internet Protocol) address** is a logical address used to identify a device's network interface and help data reach its destination on a network.

IPV4 is the type of IP Address. It stands for Internet Protocol Version 4.

Example: `192.168.1.10`
## 2. Structure of an IPv4 Address
- An IPv4 address contains **32 bits**.
- It is divided into **4 groups**.
- Each group contains **8 bits**.
- Each 8-bit group is called an **octet**.
- Dots (`.`) separate the four octets.

Example: `192.168.1.10`
- First octet: `192`
- Second octet: `168`
- Third octet: `1`
- Fourth octet: `10`
**Total bits = 4 × 8 = 32 bits**
## 3. Binary Representation
Computers represent IPv4 addresses using binary digits: `0` and `1`.

Example:
- Decimal: `192.168.1.10`
- Binary: `11000000.10101000.00000001.00001010`
Each octet has 8 bits.
## 4. Range of an Octet
An octet can have a value from **0 to 255**.

**Why?**
An octet contains 8 bits, and each bit can be either 0 or 1.

Number of possible values:
2⁸ = 256

Therefore, the possible values range from 0 to 255.

Example:
- `192.168.1.10` — valid IPv4 format.
- `192.168.1.256` — invalid because 256 is outside the allowed range for an octet.
## 5. Network ID

- The **Network ID** identifies the network to which an IP address belongs.
- It helps determine which network a device is part of.
## 6. Host ID

- The **Host ID** identifies a host or network interface within a network.
- It helps distinguish devices within that network.
## 7. Network ID vs Host ID

- **Network ID:** Identifies the network.
- **Host ID:** Identifies a host within that network.

The division between the Network ID and Host ID depends on the network prefix or subnet mask.

We cannot always determine this division by looking at the IPv4 address alone.

#