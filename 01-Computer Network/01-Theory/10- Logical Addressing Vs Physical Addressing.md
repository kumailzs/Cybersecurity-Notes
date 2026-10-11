### Why Logical Address (IP) is Essential Despite Physical Address (MAC)?
We have already physical address of a device so, why we use logical address?

These are three reasons :
### Hierarchy (Routing Efficiency)
- MAC Address is the unique flat number of a hardware so, if internet works on MAC Address so, router should store all individual MAC Address so, it's not possible to store. 
- IP Address is hierarchy (network id + host id) so, router doesn;t need to store address of every individual devices. It see only network id and forward to network.
### Mobility (Change Address When Location Change)
- MAC Address is fixed when we relocate another place. if internet works on MAC address so, when device relocated so, router should to update MAC Address
- IP Address is dynamic when we connect another network so, a new ip address assign yo  a device.
### Heterogeneous Networks (Technology Independence):
- The Layer 2 frames of different physical technologies (such as Wi-Fi, Ethernet Cable, Fiber, and Cellular 4G/5G) operate differently.
- The IP Address acts as a universal standard at Layer 3 that connects all these different hardware technologies together..
## 🔄 End-to-End Packet Flow (Summary)

When we send/receive on internet :
$$\text{Internet (Global Routing via IP)} \longrightarrow \text{Local Network (Device Identity via MAC)} \longrightarrow \text{Software Application (Process Identity via Port)}$$

1. **IP Address:** To travel data packet in internet and reached to its destination.
2. **MAC Address:** To find a specific device in a LAN.
3. **Port Address:** To send data into its specific service like Whatsapp, Yotube, and etc.