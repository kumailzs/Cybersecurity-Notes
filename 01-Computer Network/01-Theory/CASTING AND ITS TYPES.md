# Casting
**Casting** is the method of delivering data from a sender to one or more receivers over a network.
## Types of Casting
### 1. Unicast (One-to-One)
Unicast is a communication method in which data is sent from one sender to one specific receiver.
**Example:** A computer sends an HTTPS request to a web server.
### 2. Broadcast (One-to-All)
Broadcast is a communication method in which data is sent to all devices within a local broadcast domain.
**Example:** An ARP request in IPv4.

Broadcast has two types:

- **Limited Broadcast:** Uses destination IP `255.255.255.255`. It targets devices on the local network and is not forwarded by routers.
    
- **Directed Broadcast:** Targets all hosts on a specific IPv4 network using that network's broadcast address. Routers may forward it if configured to allow it, but it is usually disabled for security reasons.
**Example:** For network `192.168.2.0/24`, the directed broadcast address is `192.168.2.255`.
### 3. Multicast (One-to-Selected Group)
Multicast is a communication method in which data is sent to a specific group of receivers that are interested in receiving it.
**Example:** Delivering a live video stream to members of a multicast group.

## Comparison

| Type      | Communication                    | Example                |
| --------- | -------------------------------- | ---------------------- |
| Unicast   | One-to-One                       | HTTPS request          |
| Broadcast | One-to-All in a broadcast domain | IPv4 ARP request       |
| Multicast | One-to-Selected Group            | Multicast video stream |
