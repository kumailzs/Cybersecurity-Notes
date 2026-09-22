## Client Side Model
It's centralized architecture (authority, control, storage have one device (server)). A powerful computer (server) store data and processing. Devices send request to the server.
### For Example :
When you search on browser(client) so the request send to the google server and they respond browser then you see result.

![[Pasted image 20260917120058.png]]

## Peer to Peer Model (P2P)
It's decentralized architecture (control, authority, storage doesn't has any single device). Devices are peer (equal) that send and receive data simultaneously each other.
### For Example : 
When you send data through Bluetooth /LAN Cable device directly sharing resources without any centralized device.
![[Pasted image 20260917120532.png]]

## Confusion 

> "Look, in the client-server model, there is a centralized device that handles control, authority, and storage, and devices send requests to it. Whereas in peer-to-peer (P2P), there is no centralized system and devices both send and receive data from each other. However, our browser works on the client-server model—when we open Google Drive, the request goes to Google's server, _but_ when we upload something to Google Drive, isn't the browser actually using peer-to-peer because it can both send and receive?"

No, **uploading or downloading is bidirectional communication, which does not make it Peer-to-Peer (P2P).** Data travels in both directions (client-to-server and server-to-client) in the client-server model as well.

Here is the actual difference:
#### 1. Client-Server Model (Google Drive / Web)

- **Bidirectional?** Yes! Browsers _receive_ data when loading a page (downloading/rendering) and _send_ data when you _upload_ a file or submit a form.
- **The Real Difference:** Everything routes through a **centralized server** (`drive.google.com`).
- **Flow:** `Your Browser ⇄ Google's Server`. Your file doesn't go straight to another person's device; it goes to Google's central storage first. TCP/IP connections are full-duplex, meaning data flows both ways on the same pipe.
#### 2. Peer-to-Peer (P2P) Model

- **Bidirectional?** Yes, but with no central server or authority in the middle.
    
- **Flow:** `Your Device ⇄ Another Device (Direct IP connection)`.
    
- **Example:** BitTorrent (torrenting) or local LAN file transfer. No corporate server handles master control or storage; peers share chunks of the file directly with each other.