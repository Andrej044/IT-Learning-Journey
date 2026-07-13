I learned:
- Difference between Server Core and Desktop Experience;
- Why Domain Controllers need static IP addresses;
- VirtualBox resource allocation;
- How Windows Server installation works;


### Lab Network

- Created VB NAT Network
- Network name: BT-Lab
- IPv4 Prefix: 10.10.10.0/24   
- DHCP: Enabled
- Connected BT-DC01 to the NAT Network

## Static Network Configuration

Network Adapter:
- Renamed to LAN

IPv4:
- IP: 10.0.2.10
- Mask: 255.255.255.0
- Gateway: 10.0.2.1
- Preferred DNS: 10.0.2.10

Connectivity Tests:
- Gatewau: Success
- Internet: Success
- DNS Resolution: Success 