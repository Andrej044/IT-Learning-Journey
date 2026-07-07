If I were explaining the whole process:

I type google.com into the browser.
Windows checks its DNS cache.
If it doesn't know the IP, it sends a DNS request.
The DNS server replies with Google's IP address.
Windows realizes Google is outside the local network.
Windows needs to send the packet to the default gateway.
If it doesn't already know the router's MAC address, it uses ARP:
"Who has 192.168.2.1?"
The router replies with its MAC address.
The laptop sends the frame to the router.
The router forwards the packet toward Google.
Google sends the response back.