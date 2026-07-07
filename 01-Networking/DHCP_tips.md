DHCP stands for:
   Dynamic Host Configuration Protocol
   


Dynamic = automatically.
Host = any device on the network (laptop, phone, printer).
Configuration = network settings.
Protocol = the agreed set of rules devices use to communicate.

So DHCP is simply:

A service that automatically gives devices the network settings they need.


How device get IP(DORA)

Discover - broadcasting across network
      So it broadcasts:
         "Is there a DHCP server here? I need an IP address!"
Offer - router replies
      "Yes.
         I can give you: 192.168.2.12
         Gateway:192.168.2.1
         DNS:192.168.2.1
         Lease:8 hours."

Request- The device says:
         "Yes! I want 192.168.2.12."

Now the DHCP server knows the laptop accepted the offer.

Acknowledge - Finally the router replies:
         "Done. 192.168.2.12 is now yours."

Now the device starts using it.

Device
   │
Discover
   ▼
Router
   ▲
Offer
   │
Laptop
   │
Request
   ▼
Router
   ▲
Acknowledge
   │
Device gets IP