# TCP / UDP Overview

## General

A firewall or host will respond to a port scan in one of three ways: - Open and listening - Closed and denying - NO reply - in stealth mode

There is a potential of 65535 TCP and UDP ports. The Well-Known Ports are in the range of 0 to 1023. The most common well-known port is 80, which identifies HTTP traffic for a Web server. Registered ports are in the range 1024 to 49151. They are not assigned or controlled, but can be registered to prevent duplication.

## 3 - way handshake

TCP uses a three-way handshake to establish a reliable connection. The connection is full duplex, and both sides synchronize (SYN) and acknowledge (ACK) each other. The exchange of these four flags is performed in three steps—SYN, SYN-ACK, and ACK.

![](/images/tcp_handshake.png)
The client chooses an initial sequence number, set in the first SYN packet. The server also chooses its own initial sequence number, set in the SYN/ACK packet. Each side acknowledges each other's sequence number by incrementing it; this is the acknowledgement number. The use of sequence and acknowledgment numbers allows both sides to detect missing or out-of-order segments.

Once a connection is established, ACKs typically follow for each segment. The connection will eventually end with a RST (reset or tear down the connection) or FIN (gracefully end the connection).

No response, may indicate a firewall. You may receive an ICMP Destination Unreachable packet. The code might indicate that the network was unreachable, or the host was unreachable, but most likely, the target port is firewalled.
