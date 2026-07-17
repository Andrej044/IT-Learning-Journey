# Networking Protocols

This document describes common networking protocols, starting with basic protocols such as HTTP and TCP and moving through related transport, internet, and application layer protocols.

## Application Layer Protocols

### HTTP (Hypertext Transfer Protocol)
- Application-layer protocol used for transferring web pages and resources between clients and servers.
- Operates on top of TCP.
- Uses request methods such as GET, POST, PUT, DELETE.
- Commonly runs on ports 80 (HTTP) and 443 (HTTPS).

### HTTPS (HTTP Secure)
- HTTP over TLS/SSL.
- Encrypts data in transit to protect confidentiality and integrity.
- Widely used for secure web browsing.

### DNS (Domain Name System)
- Translates human-readable domain names to IP addresses.
- Uses both UDP and TCP on port 53.
- Includes record types such as A, AAAA, CNAME, MX, TXT.

### FTP (File Transfer Protocol)
- Application-layer protocol for transferring files between client and server.
- Uses separate control and data connections.
- Typically uses ports 20 and 21.

### SMTP (Simple Mail Transfer Protocol)
- Protocol for sending email between mail servers.
- Typically uses port 25, 587, or 465 for secure SMTP.

### SSH (Secure Shell)
- Protocol for secure remote command execution and management.
- Uses encryption and authentication over TCP port 22.

## Transport Layer Protocols

### TCP (Transmission Control Protocol)
- Connection-oriented transport protocol.
- Provides reliable, ordered, and error-checked delivery of data.
- Uses a three-way handshake to establish connections.
- Includes flow control, congestion control, and retransmission of lost packets.
- Commonly used by HTTP, HTTPS, FTP, SMTP, and many other application protocols.

### UDP (User Datagram Protocol)
- Connectionless transport protocol.
- Provides low-overhead, best-effort delivery without reliability guarantees.
- Suitable for real-time applications like DNS queries, VoIP, and streaming.
- Uses port numbers for multiplexing.

## Internet Layer Protocols

### IP (Internet Protocol)
- Core protocol for routing packets across networks.
- IPv4 uses 32-bit addresses; IPv6 uses 128-bit addresses.
- Provides packet addressing and fragmentation.

### ICMP (Internet Control Message Protocol)
- Used for network diagnostics and error reporting.
- Powers tools like ping and traceroute.
- Sends messages such as Destination Unreachable and Time Exceeded.

### ARP (Address Resolution Protocol)
- Resolves IPv4 addresses to MAC addresses on a local network.
- Operates at the boundary of the network and link layers.

## Link Layer Protocols

### Ethernet
- Common wired local area network (LAN) technology.
- Defines frame formats, MAC addressing, and physical signaling.
- Uses switches, cables, and NICs.

### Wi-Fi (IEEE 802.11)
- Wireless LAN technology.
- Provides wireless connectivity and uses MAC-layer protocols for access and security.

## Common Protocol Relationships

- HTTP and HTTPS run over TCP.
- TCP and UDP run over IP.
- DNS uses UDP for queries and TCP for larger responses or zone transfers.
- ARP works below IP to map addresses on local networks.
- ICMP helps diagnose IP connectivity issues.

## Summary

Networking protocols are organized in layers. Basic protocols like HTTP and TCP are part of the application and transport layers, while IP and link-layer protocols handle addressing and delivery. Understanding the stack helps reason about how data moves from applications to physical networks.