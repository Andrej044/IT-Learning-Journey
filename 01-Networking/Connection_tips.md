What happened when you enter google.com in your browser

Step 1
Browser ask windows - do you know IP address for google.com
Windows first check DNS cache. If it already knows, it doesn't need to ask anyone else.

Step 2 
If Windows doesn't know, it send a DNS request
Request goes to router

Step 3
Then router check if he already knows Google IP.
If not it forwards the request 
to the upstream DNS server (or another DNS resolver configured by your ISP).

Step 4

Now your browser finally knows where Google is.

It sends packets to Google's IP address.

Those packets leave your home network through your default gateway (192.168.2.1) 
and travel across many routers on the Internet until they reach Google's servers.

Step 5

Step 5️⃣

Google replies.

The response travels back through the Internet, 
reaches your router, and then your router sends it to your laptop.
Google's webpage appears.




Browser
    │
    ▼
Windows
    │
    ▼
DNS Cache?
    │
    ├── Yes → Use cached IP
    │
    └── No
          │
          ▼
Router (192.168.2.1)
          │
          ▼
DNS Server
          │
          ▼
Google IP Address
          │
          ▼
Internet
          │
          ▼
Google Server
          │
          ▼
Response
          │
          ▼
Browser
