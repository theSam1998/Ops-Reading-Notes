
# Network Protocols and Architecture
---
## Statement addressing relevance to unit:
- the reading we have been asked to do today familiarizes us with both a vital tool for port analysis and a deeper breakdown of what ports are and their functions.
## What is a port? Describe it with an analogy that would help a family member understand.
- a port is like a door into a networked device. If the port is open, the door is open, and traffic can come in and out of that door. If it is closed, it is inaccessible.
## What does a port scanner send to a port to check the current status?
- a packet of network data.
## When a port scanner sends a request to connect,
 what are the three possible responses? Describe them.
- SYN-ACK, no response, or RST. RST means there is a live computer at that address, but the port is closed. SYN-ACK is likely an open port. No response indicates SYN filtering on the network.
## What is the difference between TCP and UDP?
- Transmission Control Protocol sends each packet in order with error checking via three way handshake for each step. This ensures data is transmitted properly. User Datagram Protocol, on the other hand, does not feature error checking but is much faster than TCP.
## List and describe the ports used for the following:
- Telnet: tcp port 23, same as ssh but unencrypted. 
- SSH: tcp port 22, secure shell connection for encrypted connection from one shell to another. Allows for remote access to shell.
- DNS: translates web address names into IP addresses, operates on udp port 53 or TCP port 53 in the case of larger amounts of data.
- SMTP: server to server communication commonly used for sending emails, operates on TCP port 25. If using tls encrypted smtp, operates on TCP port 587. This is used for sending emails to their destinations. IMAP and pop3 are used for inbound email, and communicate over tcp ports 143 and 110 respectively. Tls encrypted versions use tcp ports 993 and 995
- HTTP: uses TCP port 80, used for communicating with a webserver (e.g. accessing a website.)
- HTTPS: same as http but encrypted, uses port 443. Most websites today use https.
- RDP: provides GUI based view of a remote desktop, uses tcp port 3389
- Ping: a ping tests ICMP, which does not use ports, so no port is used. ICMP sits on top of the IP, so it is simply a test if the device is accessible from that network.
